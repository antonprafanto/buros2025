# DESAIN PROSES DAN MODEL EKOSISTEM HIDUP
## Sistem Sensor LiDAR Anti-Collision untuk Tugboat

---

## 1. DIAGRAM ARSITEKTUR SISTEM

### 1.1 Arsitektur Tiga Lapis (Three-Layer Architecture)

```
╔══════════════════════════════════════════════════════════════════╗
║                        LAYER 3: OUTPUT/INTERFACE                  ║
║                                                                   ║
║  ┌─────────────┐  ┌──────────────┐  ┌────────────────────────┐  ║
║  │ LCD Display │  │ LED Indicator│  │  Audio Alarm System    │  ║
║  │  (Jarak &   │  │ (G/Y/R LED)  │  │  (Buzzer Bertingkat)   │  ║
║  │   Status)   │  │              │  │                        │  ║
║  └──────┬──────┘  └──────┬───────┘  └───────────┬────────────┘  ║
║         │                │                      │                ║
║         └────────────────┴──────────────────────┘                ║
╚═════════════════════════════════╪════════════════════════════════╝
                                  │
╔═════════════════════════════════╪════════════════════════════════╗
║                    LAYER 2: PROCESSING UNIT                       ║
║                                 │                                 ║
║         ┌───────────────────────▼─────────────────────┐           ║
║         │     Mikrokontroler (Arduino/Raspberry Pi)   │           ║
║         │                                             │           ║
║         │  ┌─────────────────────────────────────┐    │           ║
║         │  │   Data Acquisition Module           │   │           ║
║         │  │   - Serial Communication (UART/CAN) │   │           ║
║         │  │   - Data Parsing & Validation       │   │           ║
║         │  └─────────────────────────────────────┘   │           ║
║         │                                             │           ║
║         │  ┌─────────────────────────────────────┐   │           ║
║         │  │   Signal Processing Algorithm       │   │           ║
║         │  │   - Distance Calculation            │   │           ║
║         │  │   - Noise Filtering                 │   │           ║
║         │  │   - Multi-sensor Fusion             │   │           ║
║         │  └─────────────────────────────────────┘   │           ║
║         │                                             │           ║
║         │  ┌─────────────────────────────────────┐   │           ║
║         │  │   Decision Logic Engine             │   │           ║
║         │  │   - Zone Classification             │   │           ║
║         │  │   - Threshold Comparison            │   │           ║
║         │  │   - Alert Level Determination       │   │           ║
║         │  └─────────────────────────────────────┘   │           ║
║         │                                             │           ║
║         │  ┌─────────────────────────────────────┐   │           ║
║         │  │   Data Logging System               │   │           ║
║         │  │   - SD Card Storage                 │   │           ║
║         │  │   - Timestamp Recording             │   │           ║
║         │  └─────────────────────────────────────┘   │           ║
║         └─────────────────────────────────────────────┘           ║
║                                 ▲                                 ║
╚═════════════════════════════════╪════════════════════════════════╝
                                  │
╔═════════════════════════════════╪════════════════════════════════╗
║                      LAYER 1: SENSOR INPUT                        ║
║                                 │                                 ║
║  ┌──────────────────────────────┴────────────────────────────┐   ║
║  │                   Sensor Integration                       │   ║
║  └─────────┬────────────────────────────────────┬─────────────┘   ║
║            │                                    │                 ║
║  ┌─────────▼──────────┐             ┌──────────▼──────────────┐  ║
║  │  TF03 LiDAR        │             │  TFA300-L LiDAR         │  ║
║  │  (Sensor Primer)   │             │  (Sensor Sekunder)      │  ║
║  │                    │             │                         │  ║
║  │  • Range: 180m     │             │  • Range: 290m          │  ║
║  │  • Freq: 100Hz     │             │  • Freq: 10,000Hz       │  ║
║  │  • FOV: 0.5°       │             │  • FOV: 0.5°            │  ║
║  │  • IP67 Rating     │             │  • Weight: 10.5g        │  ║
║  │  • UART/CAN        │             │  • UART/CAN             │  ║
║  └────────────────────┘             └─────────────────────────┘  ║
║                                                                   ║
║            Mounting Position: Bow (Haluan) Tugboat                ║
╚═══════════════════════════════════════════════════════════════════╝
```

---

## 2. FLOWCHART PROSES OPERASIONAL

```
                        ┌─────────────────┐
                        │  START SYSTEM   │
                        │  (Engine ON)    │
                        └────────┬────────┘
                                 │
                        ┌────────▼────────┐
                        │ Sensor Init &   │
                        │  Self-Check     │
                        └────────┬────────┘
                                 │
                         ┌───────▼───────┐
                         │ Sensor Ready? │
                         └───┬───────┬───┘
                             │ NO    │ YES
                    ┌────────▼────┐  │
                    │ Error Alert │  │
                    │  (Buzzer)   │  │
                    └─────────────┘  │
                                     │
                  ┌──────────────────▼──────────────────┐
                  │  Continuous Scanning (100Hz/10KHz)  │
                  └──────────────────┬──────────────────┘
                                     │
                           ┌─────────▼─────────┐
                           │ Object Detected?  │
                           └─────┬──────┬──────┘
                                 │ NO   │ YES
                         ┌───────▼─┐    │
                         │ Display │    │
                         │  "AMAN" │    │
                         │ (Green) │    │
                         └─────────┘    │
                                        │
                           ┌────────────▼──────────────┐
                           │ Measure Distance (meter)  │
                           └────────────┬──────────────┘
                                        │
                        ┌───────────────▼───────────────┐
                        │     Zone Classification       │
                        └──┬──────────┬─────────────┬───┘
                           │          │             │
        ┌──────────────────▼────┐  ┌──▼───────┐  ┌─▼────────────┐
        │ ZONA AMAN             │  │  ZONA    │  │  ZONA BAHAYA │
        │ Distance > 100m       │  │ WASPADA  │  │ Distance < 50m│
        │                       │  │ 50-100m  │  │              │
        │ • Display: Green      │  │          │  │• Display: Red│
        │ • LED: Green          │  │• Display:│  │• LED: Red    │
        │ • Alarm: OFF          │  │  Yellow  │  │• Alarm: FAST │
        │ • Action: Normal Nav  │  │• LED:    │  │• Action:     │
        │                       │  │  Yellow  │  │  EVASIVE     │
        └───────────────────────┘  │• Alarm:  │  │  MANEUVER    │
                                   │  SLOW    │  │              │
                                   │  BEEP    │  └──────────────┘
                                   │• Action: │
                                   │  CAUTION │
                                   └──────────┘
                                        │
                  ┌─────────────────────┴─────────────────────┐
                  │  Log Data (timestamp, distance, zone)     │
                  └─────────────────────┬─────────────────────┘
                                        │
                           ┌────────────▼──────────────┐
                           │  Continue Scanning Loop   │
                           │  (Return to Scanning)     │
                           └───────────────────────────┘
```

---

## 3. MODEL EKOSISTEM HIDUP (LIVING LAB ECOSYSTEM)

### 3.1 Stakeholder Mapping

```
                    ┌────────────────────────────────────┐
                    │    PEMERINTAH (REGULATOR)          │
                    │                                    │
                    │  • Kementerian Perhubungan         │
                    │  • Direktorat Jenderal Perhubungan │
                    │    Laut (DJPL)                     │
                    │  • KSOP Samarinda (MITRA UTAMA)    │
                    └──────────────┬─────────────────────┘
                                   │
                    ┌──────────────▼──────────────┐
                    │   KOORDINASI & REGULASI     │
                    └──────────────┬──────────────┘
                                   │
    ┌──────────────────────────────┼──────────────────────────────┐
    │                              │                              │
┌───▼──────────────┐    ┌──────────▼─────────┐    ┌─────────────▼────────┐
│  PENELITI        │    │  OPERATOR TUGBOAT  │    │  INDUSTRI MARITIM    │
│  (PERGURUAN      │◄───┤  (END USER)        │◄───┤  (ADOPTER)           │
│   TINGGI)        │    │                    │    │                      │
│                  │    │ • Nahkoda          │    │ • Perusahaan         │
│ • Tim Riset      │───►│ • Awak Kapal       │───►│   Pelayaran          │
│ • Laboratorium   │    │ • Teknisi          │    │ • Pemilik Armada     │
│ • Mahasiswa      │    │                    │    │ • Mitra Bisnis       │
└──────┬───────────┘    └─────────┬──────────┘    └──────────┬───────────┘
       │                          │                          │
       │                          │                          │
       └──────────┬───────────────┴─────────────┬────────────┘
                  │                             │
       ┌──────────▼──────────────┐   ┌──────────▼───────────────┐
       │  KNOWLEDGE CREATION     │   │  TECHNOLOGY TRANSFER     │
       │  (Riset & Publikasi)    │   │  (Adopsi & Scale-up)     │
       └─────────────────────────┘   └──────────────────────────┘
```

### 3.2 Interaksi Ekosistem (Ecosystem Interaction Flow)

| Stakeholder | Kontribusi (Input) | Manfaat (Output) | Mekanisme Kolaborasi |
|-------------|-------------------|------------------|----------------------|
| **Perguruan Tinggi** | • Expertise teknologi<br>• Fasilitas riset<br>• SDM peneliti | • Publikasi ilmiah<br>• Hak kekayaan intelektual<br>• Pengalaman praktis mahasiswa | • Memorandum of Understanding (MoU)<br>• Co-supervision penelitian<br>• Joint workshop |
| **KSOP Samarinda** | • Akses lapangan<br>• Data kecelakaan<br>• Regulasi & standar<br>• Izin operasional | • Teknologi untuk monitoring<br>• Rekomendasi kebijakan<br>• Peningkatan keselamatan | • Koordinasi bulanan<br>• Site visit bersama<br>• Validasi sistem |
| **Operator Tugboat** | • Insight operasional<br>• Feedback user<br>• Partisipasi uji coba | • Peningkatan keselamatan<br>• Kompetensi teknologi<br>• Sertifikat pelatihan | • User testing session<br>• Interview mendalam<br>• Pelatihan hands-on |
| **Industri Maritim** | • Dukungan finansial<br>• Akses armada<br>• Network bisnis | • Inovasi kompetitif<br>• CSR program<br>• First mover advantage | • Pilot project sponsorship<br>• Technology licensing<br>• Business matching |

### 3.3 Living Lab Cycle

```
    1. CO-CREATION                    2. CO-DESIGN
    ┌─────────────┐                  ┌─────────────┐
    │ Identifikasi│                  │   Desain    │
    │  Kebutuhan  │─────────────────►│   Sistem    │
    │  Bersama    │                  │  Bersama    │
    └─────────────┘                  └──────┬──────┘
          ▲                                 │
          │                                 │
          │                                 ▼
    4. CO-EVALUATION              3. CO-IMPLEMENTATION
    ┌─────────────┐                  ┌─────────────┐
    │  Evaluasi   │                  │    Uji      │
    │  & Iterasi  │◄─────────────────│   Coba      │
    │  Bersama    │                  │  Lapangan   │
    └─────────────┘                  └─────────────┘
```

**Penjelasan Cycle:**

1. **Co-Creation**: Workshop dengan stakeholders untuk mengidentifikasi pain points dan kebutuhan sebenarnya operator tugboat.

2. **Co-Design**: Melibatkan operator dalam proses desain interface dan pengaturan threshold alarm untuk memastikan usability.

3. **Co-Implementation**: Uji coba bersama di lapangan dengan monitoring real-time dan dukungan teknis tim peneliti.

4. **Co-Evaluation**: Review performa sistem bersama seluruh stakeholders, iterasi improvement berdasarkan feedback.

---

## 4. DEPLOYMENT MODEL

### 4.1 Fase Deployment

```
FASE 1: PILOT PROJECT (Bulan 6-7)
┌────────────────────────────────────────────┐
│ • 2 Tugboat Pilot                          │
│ • Rute: Samarinda - Tenggarong (50 km)    │
│ • Durasi: 1 bulan intensive testing        │
│ • Tim monitoring: On-site daily            │
└────────────────────────────────────────────┘
                    │
                    ▼
FASE 2: EARLY ADOPTION (Bulan 8-12)
┌────────────────────────────────────────────┐
│ • 5 Tugboat Additional                     │
│ • Rute: Expanded (Samarinda - Muara Kaman)│
│ • Support: Remote monitoring               │
│ • Feedback: Weekly collection              │
└────────────────────────────────────────────┘
                    │
                    ▼
FASE 3: SCALE-UP (Tahun 2-3)
┌────────────────────────────────────────────┐
│ • Target: 20+ Tugboat                      │
│ • Coverage: Seluruh Sungai Mahakam         │
│ • Business Model: Technology licensing     │
│ • Support: Distributor lokal               │
└────────────────────────────────────────────┘
```

### 4.2 Sustainability Model

**Keberlanjutan Teknologi:**
- Maintenance protocol dengan spare parts availability
- Technical support hotline (24/7 emergency contact)
- Annual calibration service

**Keberlanjutan Finansial:**
- Grant funding untuk fase pilot (BESTARI SAINTEK)
- Cost-sharing dengan operator untuk fase adoption
- Commercialization path: licensing kepada vendor maritim

**Keberlanjutan Kelembagaan:**
- Pembentukan "Maritime Technology Innovation Hub" di institusi peneliti
- Partnership agreement jangka panjang dengan KSOP
- Community of practice untuk operator tugboat

---

## 5. RISK MITIGATION MATRIX

| Risiko | Dampak | Probabilitas | Mitigasi | Owner |
|--------|--------|--------------|----------|-------|
| Sensor rusak karena kondisi ekstrem | HIGH | MEDIUM | • Casing IP67<br>• Sensor backup<br>• Asuransi peralatan | Tim Peneliti |
| Resistensi operator terhadap teknologi baru | MEDIUM | HIGH | • Pelatihan intensif<br>• Demonstrasi manfaat<br>• Incentive early adopter | Tim + KSOP |
| False positive alarm (alarm palsu) | MEDIUM | MEDIUM | • Algoritma filtering<br>• Threshold tuning<br>• User override option | Tim Software |
| Keterbatasan budget | HIGH | LOW | • Phased approach<br>• Buffer 15%<br>• Alternative sourcing | Ketua Tim |
| Delay pengadaan komponen | MEDIUM | MEDIUM | • Early procurement<br>• Multiple supplier<br>• Local substitute | Logistik Tim |

---

## 6. MONITORING & EVALUATION FRAMEWORK

### Key Performance Indicators (KPI)

**Technical Performance:**
- Detection Accuracy: Target ≥ 95%
- Response Time: Target ≤ 0.1 second
- System Uptime: Target ≥ 98%
- False Positive Rate: Target ≤ 5%

**Usability Performance:**
- User Satisfaction Score: Target ≥ 8/10
- Training Success Rate: Target 100% operator trained
- System Adoption Rate: Target 70% willing to continue use

**Impact Performance:**
- Near-Miss Incident Reduction: Target -40% (Year 1)
- Operator Confidence Level: Target +50% (self-reported)
- Actual Accident Reduction: Target -30% (Year 2-3)

### Data Collection Methods

1. **Automatic Data Logging**: Setiap deteksi objek tercatat dengan timestamp, distance, zone
2. **Operator Survey**: Questionnaire pre-post deployment untuk mengukur satisfaction dan confidence
3. **KSOP Incident Report**: Comparative analysis kecelakaan sebelum dan sesudah implementasi
4. **Focus Group Discussion**: Setiap 3 bulan untuk gathering qualitative feedback

---

**DESAIN PROSES DAN MODEL EKOSISTEM INI DISUSUN BERDASARKAN KONSEP LIVING LAB YANG MENEKANKAN KOLABORASI MULTI-STAKEHOLDER DAN ITERASI BERKELANJUTAN UNTUK MEMASTIKAN SOLUSI TEKNOLOGI TEPAT GUNA DAN BERKELANJUTAN**
