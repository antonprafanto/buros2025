# KERANGKA LOGIS (LOGIC MODEL) / TEORI PERUBAHAN (THEORY OF CHANGE)
## Sistem Sensor LiDAR Anti-Collision untuk Tugboat - Sungai Mahakam Samarinda

---

## 1. LOGIC MODEL FRAMEWORK

```
INPUT ──► ACTIVITIES ──► OUTPUT ──► OUTCOME ──► IMPACT
 (Apa    (Apa yang     (Apa hasil  (Perubahan  (Dampak
  yang     kita         langsung    jangka      jangka
  kita     lakukan?)    yang        pendek)     panjang)
  punya?)              dihasilkan?)
```

---

## 2. DETAIL LOGIC MODEL

### 2.1 INPUT (Sumber Daya)

#### A. Sumber Daya Manusia

| Kategori | Jumlah | Peran | Komitmen Waktu |
|----------|--------|-------|----------------|
| **Ketua Peneliti** | 1 orang | Project coordinator, system architect | Full-time (9 bulan) |
| **Peneliti Anggota 1** | 1 orang | Software developer, algorithm engineer | Full-time (9 bulan) |
| **Peneliti Anggota 2** | 1 orang | Field coordinator, maritime liaison | Part-time (6 bulan) |
| **Asisten Peneliti** | 2 orang | Technical support, data collection | Part-time (9 bulan) |
| **Mahasiswa** | 2 orang | Assembly, testing, documentation | Part-time (6 bulan) |
| **Koordinator KSOP** | 1 orang | Field access facilitator, validator | Advisor (9 bulan) |
| **Operator Tugboat** | 20 orang | Testing participant, feedback provider | On-demand (2 bulan) |

**Total Human Resources**: 28 orang dengan berbagai tingkat komitmen

#### B. Sumber Daya Material & Peralatan

| Item | Spesifikasi | Quantity | Fungsi |
|------|-------------|----------|--------|
| **TF03 LiDAR** | 180m range, IP67, 1KHz | 8 unit | Multi-angle collision detection (depan 4x, samping 2x, sudut 2x) |
| **TFA300-L LiDAR** | 290m range, 10KHz | 3 unit | Long-range detection (depan center 2x, belakang 1x) |
| **Raspberry Pi 4** | 8GB RAM | 1 unit | Master controller untuk 10-sensor fusion |
| **Arduino Mega** | 2560 | 3 unit | Sensor interface & data acquisition |
| **LCD Touchscreen** | 7" TFT Waterproof | 1 unit | Real-time visualization & control interface |
| **LED Indicator** | RGB LED array | 3 set | Multi-zone status indicator (depan/samping/belakang) |
| **Buzzer/Alarm** | Multi-tone 90dB waterproof | 2 unit | Multi-level audio warning system |
| **Power Supply** | 12V DC converter + 20Ah battery + BMS | 1 set | High-capacity power management |
| **Waterproof Enclosure** | IP67 large enclosure | 1 unit | Main component protection |
| **Mounting Bracket** | Stainless adjustable + damper | 10 set | Individual sensor mounting with vibration damping |
| **SD Card Module** | 64GB high-speed microSD | 1 unit | High-capacity data logging |
| **Kabel & Connector** | Marine-grade shielded IP68 | 50m + 30 unit | Heavy-duty electrical connection |
| **3D Printer** | Creality K2 PLUS CFS Combo + Filamen | 1 set | Multi-material rapid prototyping, AI cameras, 350mm³ build |
| **Development Tools** | Laptop, oscilloscope, logic analyzer, soldering station | 1 set | Professional development & testing |

#### C. Sumber Daya Finansial (Budget Estimasi)

**Total Budget**: **Rp 289.900.000**

| Kategori Biaya | Estimasi (IDR) | Persentase |
|----------------|----------------|------------|
| **A. Sensor & Komponen Import (10 Sensor System)** | | |
| • Sensor LiDAR (8x TF03 + 3x TFA300-L) | Rp 64.461.000 | 22,2% |
| • Mikrokontroler & Processing Module | Rp 7.152.000 | 2,5% |
| • Display, Alarm & Interface | Rp 2.708.000 | 0,9% |
| • Power Supply & Battery System | Rp 4.105.000 | 1,4% |
| • Enclosure & Mounting Hardware | Rp 10.495.000 | 3,6% |
| • Kabel, Konektor & Wiring | Rp 14.813.000 | 5,1% |
| • Komponen Elektronik Pendukung | Rp 5.568.000 | 1,9% |
| **Subtotal Import** | **Rp 109.302.000** | **37,7%** |
| | | |
| **B. Bea Cukai & Pajak Impor** | **Rp 33.173.000** | **11,4%** |
| | | |
| **C. Tools, Equipment & 3D Printing** | | |
| • Creality K2 PLUS CFS Combo 3D Printer | Rp 31.721.000 | 10,9% |
| • Filamen (PLA, PETG, TPU) & Accessories | Rp 5.820.000 | 2,0% |
| • Soldering, Testing & Assembly Tools | Rp 15.553.000 | 5,4% |
| **Subtotal Tools** | **Rp 53.094.000** | **18,3%** |
| | | |
| **D. Operasional Lapangan & Safety Equipment** | | |
| • Instalasi & Field Testing | Rp 15.871.000 | 5,5% |
| • Safety Equipment / PPE (K3 Standar Industri) | Rp 38.140.000 | 13,2% |
| • Pelatihan & Dokumentasi | Rp 11.215.000 | 3,9% |
| **Subtotal Operasional** | **Rp 65.226.000** | **22,5%** |
| | | |
| **E. Contingency & Miscellaneous** | **Rp 29.105.000** | **10,0%** |
| | | |
| **TOTAL BUDGET** | **Rp 289.900.000** | **100%** |

**Rincian Bea Cukai & Pajak Impor**:
- Bea Masuk (10%): Rp 10.930.000
- PPN Impor (11%): Rp 13.225.000
- PPh Pasal 22 Impor (7,5%): Rp 9.018.000
- **Total Bea Cukai & Pajak**: Rp 33.173.000

**Catatan**:
1. **Sistem 10 Sensor LiDAR**: Konfigurasi 8x TF03 (180m) + 3x TFA300-L (290m) untuk 360° coverage dengan density tinggi pada bagian depan kapal
2. **Creality K2 PLUS CFS Combo**: Multi-material 3D printer dengan Dual AI cameras, build volume 350x350x350mm, max speed 600mm/s untuk rapid prototyping enclosure, mounting bracket, dan komponen custom
3. **Safety Equipment (PPE)**: Standar industri lengkap meliputi kacamata safety, masker N95, helmet ANSI-certified, life jacket USCG-approved, safety shoes steel toe, fall protection harness, first aid kit maritime, dan APAR
4. **Biaya Sewa Tugboat**: TIDAK termasuk dalam budget (kolaborasi dengan operator lokal melalui Living Lab approach)
5. Budget mencakup komponen pendukung lengkap: enclosure waterproof IP67, kabel marine-grade shielded, mounting bracket stainless adjustable, vibration damper
6. Tools professional: soldering station, multimeter, oscilloscope 100MHz, logic analyzer, crimping tools, power drill
7. Potensi pembebasan/keringanan bea masuk untuk institusi pendidikan (konsultasi Bea Cukai)

#### D. Sumber Daya Waktu

- **Durasi Total Penelitian**: 9 bulan
- **Fase Persiapan**: 2 bulan
- **Fase Pengembangan**: 3 bulan
- **Fase Uji Coba**: 2 bulan
- **Fase Finalisasi**: 2 bulan

#### E. Sumber Daya Infrastruktur

- Laboratorium elektronika perguruan tinggi
- Workshop untuk assembly dan testing
- Akses lapangan Sungai Mahakam via KSOP
- Fasilitas tugboat untuk instalasi uji coba

---

### 2.2 ACTIVITIES (Aktivitas)

#### Phase 1: Persiapan dan Desain (Bulan 1-2)

| Aktivitas | Sub-Aktivitas | Output Spesifik |
|-----------|---------------|-----------------|
| **Kick-off Meeting** | • Koordinasi dengan KSOP<br>• Alignment ekspektasi<br>• Pembagian tugas tim | MoU dengan KSOP, Work Breakdown Structure |
| **Studi Lapangan** | • Observasi operasional tugboat<br>• Interview nahkoda dan operator<br>• Survey kondisi Sungai Mahakam | Field observation report, User requirement document |
| **Desain Sistem** | • Arsitektur hardware<br>• Flowchart algoritma<br>• Interface mockup | System design document, Technical specification |
| **Procurement** | • Pembelian sensor LiDAR<br>• Pengadaan komponen<br>• Verifikasi kualitas | All materials ready, Quality check report |

#### Phase 2: Pengembangan Prototype (Bulan 3-5)

| Aktivitas | Sub-Aktivitas | Output Spesifik |
|-----------|---------------|-----------------|
| **Hardware Assembly** | • Integrasi sensor dengan MCU<br>• Wiring dan soldering<br>• Mounting system fabrication | Prototype hardware v1.0 |
| **Software Development** | • Firmware programming (C/Python)<br>• Algorithm implementation<br>• Interface development | Source code, Executable firmware |
| **Lab Testing** | • Unit testing per komponen<br>• Integration testing sistem<br>• Stress testing (24 jam kontinyu) | Test report, Bug list |
| **Kalibrasi** | • Distance accuracy calibration<br>• Threshold tuning<br>• Response time optimization | Calibration certificate, Performance metrics |

#### Phase 3: Uji Coba Lapangan (Bulan 6-7)

| Aktivitas | Sub-Aktivitas | Output Spesifik |
|-----------|---------------|-----------------|
| **Instalasi di Tugboat** | • Mounting sensor di bow<br>• Electrical connection<br>• Display installation di wheelhouse | 2 tugboat equipped with system |
| **Field Testing** | • Operasional normal (daily route)<br>• Various weather conditions<br>• Day and night operations | Field test log, Performance data |
| **Data Collection** | • Automatic data logging<br>• Operator feedback interview<br>• Video documentation | Data log (100+ hours), Interview transcript |
| **Monitoring & Support** | • On-site technical support<br>• Real-time troubleshooting<br>• Daily performance check | Support log, Issue tracker |

#### Phase 4: Evaluasi dan Improvement (Bulan 8)

| Aktivitas | Sub-Aktivitas | Output Spesifik |
|-----------|---------------|-----------------|
| **Data Analysis** | • Statistical analysis akurasi<br>• False positive rate calculation<br>• User satisfaction scoring | Analysis report, Statistics dashboard |
| **System Improvement** | • Bug fixing<br>• Algorithm optimization<br>• Interface enhancement | Prototype v2.0 (final version) |
| **Re-testing** | • Validation testing<br>• Comparative before-after | Validation report, Improvement metrics |

#### Phase 5: Finalisasi dan Diseminasi (Bulan 9)

| Aktivitas | Sub-Aktivitas | Output Spesifik |
|-----------|---------------|-----------------|
| **Dokumentasi** | • User manual (Bahasa Indonesia)<br>• Technical documentation<br>• Maintenance guide | Complete documentation package |
| **Pelatihan Massal** | • Training workshop (20 operator)<br>• Hands-on practice<br>• Certification test | Training certificate, Training report |
| **Publikasi** | • Paper writing<br>• Submission ke jurnal<br>• Conference presentation | Scientific paper, Presentation slides |
| **Seminar Hasil** | • Stakeholder gathering<br>• Technology showcase<br>• Recommendation handover to KSOP | Seminar report, KSOP recommendation letter |

---

### 2.3 OUTPUT (Hasil Langsung)

| No | Output | Deskripsi | Indikator Keberhasilan |
|----|--------|-----------|------------------------|
| **O1** | **Prototype Fungsional** | 1 unit sistem 10-sensor LiDAR anti-collision fully operational | ✓ Detection range ≥290m (long-range)<br>✓ 360° coverage tanpa blind spot<br>✓ Accuracy ±10cm<br>✓ Response time ≤0.1s<br>✓ Uptime ≥98%<br>✓ Multi-sensor fusion berhasil |
| **O2** | **Dokumentasi Teknis** | Manual lengkap dalam Bahasa Indonesia | ✓ Installation guide (min 10 halaman)<br>✓ User manual (min 15 halaman)<br>✓ Maintenance guide (min 8 halaman) |
| **O3** | **Data Lapangan** | Log deteksi dari uji coba operasional | ✓ Minimal 100 jam data<br>✓ Minimal 1000 deteksi events<br>✓ Data integrity 100% |
| **O4** | **Operator Terlatih** | SDM kompeten mengoperasikan sistem | ✓ 20 operator certified<br>✓ Post-training score ≥80/100<br>✓ Retention rate 100% |
| **O5** | **Publikasi Ilmiah** | Diseminasi hasil penelitian | ✓ 1 artikel jurnal nasional terakreditasi<br>✓ 1 prosiding seminar internasional<br>✓ 1 laporan akhir penelitian |
| **O6** | **Rekomendasi KSOP** | Endorsement dari mitra | ✓ Surat rekomendasi resmi KSOP<br>✓ Approval untuk implementasi lanjutan |

---

### 2.4 OUTCOME (Hasil Jangka Pendek: 1-2 Tahun)

| Outcome | Indikator | Baseline | Target Year 1 | Target Year 2 | Metode Pengukuran |
|---------|-----------|----------|---------------|---------------|-------------------|
| **OC1: Peningkatan Kesadaran Situasional Operator** | Situational awareness score | 5.5/10 (pre-survey) | 8.0/10 | 8.5/10 | Operator self-assessment questionnaire |
| **OC2: Adopsi Teknologi** | Jumlah tugboat menggunakan sistem | 0 unit | 5 unit (pilot + adoption) | 15 unit | KSOP deployment registry |
| **OC3: Pengurangan Near-Miss Incidents** | Jumlah insiden hampir tabrakan per bulan | 12 insiden/bulan (baseline KSOP data) | 7 insiden/bulan (-40%) | 5 insiden/bulan (-58%) | KSOP incident report analysis |
| **OC4: Peningkatan Response Time** | Waktu reaksi operator saat deteksi objek | 5 detik (tanpa sistem) | 2 detik (dengan sistem) | 1.5 detik | Data log analysis |
| **OC5: Confidence Level Operator** | Tingkat kepercayaan diri operator | 6.0/10 (pre-survey) | 8.5/10 | 9.0/10 | Pre-post survey comparison |
| **OC6: Standarisasi Prosedur** | Ketersediaan SOP penggunaan sensor | Tidak ada | SOP draft | SOP official (KSOP decree) | Document verification |

#### Pathway: Output → Outcome

```
OUTPUT                           MECHANISMS                      OUTCOME
┌──────────────────┐           ┌──────────────────┐           ┌─────────────────┐
│ Prototype        │           │ • System provides│           │ Situational     │
│ Fungsional       │──────────►│   real-time data │──────────►│ Awareness       │
│ (O1)             │           │ • Visual & audio │           │ Meningkat (OC1) │
└──────────────────┘           │   alert          │           └─────────────────┘
                               └──────────────────┘

┌──────────────────┐           ┌──────────────────┐           ┌─────────────────┐
│ Operator         │           │ • Training builds│           │ Confidence &    │
│ Terlatih         │──────────►│   competency     │──────────►│ Competency      │
│ (O4)             │           │ • Hands-on skill │           │ Meningkat (OC5) │
└──────────────────┘           └──────────────────┘           └─────────────────┘

┌──────────────────┐           ┌──────────────────┐           ┌─────────────────┐
│ Rekomendasi      │           │ • KSOP endorses  │           │ Technology      │
│ KSOP             │──────────►│   technology     │──────────►│ Adoption        │
│ (O6)             │           │ • Policy support │           │ Expanded (OC2)  │
└──────────────────┘           └──────────────────┘           └─────────────────┘

┌──────────────────┐           ┌──────────────────┐           ┌─────────────────┐
│ Data Lapangan &  │           │ • Evidence-based │           │ Near-Miss       │
│ Performance      │──────────►│   improvement    │──────────►│ Incidents       │
│ Metrics (O3)     │           │ • Feedback loop  │           │ Reduced (OC3)   │
└──────────────────┘           └──────────────────┘           └─────────────────┘
```

---

### 2.5 IMPACT (Dampak Jangka Panjang: 3-5 Tahun)

#### Strategic Impact Goals

| Impact Area | Deskripsi | Indikator | Target 5 Tahun |
|-------------|-----------|-----------|----------------|
| **I1: Keselamatan Maritim** | Penurunan signifikan kecelakaan navigasi di Sungai Mahakam | • Jumlah kecelakaan tabrakan/tahun<br>• Fatality rate<br>• Property damage value | • -50% accident rate<br>• -70% fatality<br>• -60% damage cost |
| **I2: Efisiensi Operasional** | Peningkatan produktivitas dan confidence operator | • Downtime akibat insiden<br>• Trip delay frequency<br>• Operator retention rate | • -40% downtime<br>• -50% delay<br>• +30% retention |
| **I3: Replikasi Regional** | Adopsi teknologi di sungai-sungai besar Indonesia | • Jumlah sungai implementasi<br>• Jumlah provinsi adopsi<br>• Jumlah tugboat total | • 5 sungai major<br>• 10 provinsi<br>• 100+ tugboat |
| **I4: Kontribusi Kebijakan** | Influencing regulasi keselamatan maritim sungai | • Regulasi baru terkait sensor safety<br>• Standar nasional (SNI)<br>• Integrasi ke kurikulum pelatihan | • 1 Permenhub baru<br>• 1 SNI proposal<br>• Adopsi di 5 training center |
| **I5: Ekosistem Inovasi** | Pembentukan kluster inovasi teknologi maritim | • Startup/UMKM di bidang maritime tech<br>• Partnership industri-akademisi<br>• Publikasi & patent | • 3 startup baru<br>• 5 MoU industri<br>• 5 publikasi + 1 paten |

#### Theory of Change: Pathway to Impact

```
┌─────────────────────────────────────────────────────────────────────────┐
│                        ULTIMATE IMPACT (Vision)                         │
│                                                                         │
│   "Transportasi sungai di Indonesia yang AMAN, EFISIEN, dan           │
│    BERKELANJUTAN melalui adopsi teknologi sensor anti-collision"       │
└─────────────────────────────────────────────────────────────────────────┘
                                    ▲
                                    │
                     ┌──────────────┴───────────────┐
                     │                              │
┌────────────────────▼──────────┐   ┌──────────────▼─────────────────┐
│ LONG-TERM OUTCOME (3-5 Tahun) │   │ SYSTEMIC CHANGE                │
│                                │   │                                │
│ • Normalisasi penggunaan       │   │ • Regulasi mendukung           │
│   sensor pada tugboat          │   │ • Standarisasi teknologi       │
│ • Budaya safety consciousness  │   │ • Ekosistem inovasi mature     │
│ • Industri maritim kompetitif  │   │ • Supply chain lokal terbentuk │
└────────────────────────────────┘   └────────────────────────────────┘
                     ▲                              ▲
                     │                              │
                     └──────────────┬───────────────┘
                                    │
┌───────────────────────────────────▼─────────────────────────────────────┐
│                    INTERMEDIATE OUTCOME (1-2 Tahun)                     │
│                                                                          │
│ • Adoption oleh 15 tugboat                                              │
│ • Near-miss reduction 40-58%                                            │
│ • SOP resmi dari KSOP                                                   │
│ • Operator trained dan confident                                        │
└───────────────────────────────────▲─────────────────────────────────────┘
                                    │
                     ┌──────────────┴───────────────┐
                     │                              │
┌────────────────────▼──────────┐   ┌──────────────▼─────────────────┐
│ IMMEDIATE OUTPUT (9 Bulan)    │   │ ENABLING FACTORS               │
│                                │   │                                │
│ • 1 Prototype 10-sensor system │   │ • Support KSOP penuh           │
│ • 20 Operator trained          │   │ • Budget adequate              │
│ • Documentation complete       │   │ • Tim kompeten                 │
│ • KSOP recommendation          │   │ • Teknologi proven             │
└────────────────────────────────┘   └────────────────────────────────┘
                     ▲                              ▲
                     │                              │
                     └──────────────┬───────────────┘
                                    │
┌───────────────────────────────────▼─────────────────────────────────────┐
│                            ACTIVITIES (9 Bulan)                          │
│                                                                          │
│ Desain → Develop → Testing → Field Trial → Evaluation → Dissemination  │
└──────────────────────────────────────────────────────────────────────────┘
                                    ▲
                                    │
┌───────────────────────────────────▼─────────────────────────────────────┐
│                             INPUT (Resources)                            │
│                                                                          │
│ SDM (28 orang) + 10 Sensor LiDAR System + Budget (Rp 289,9jt) +        │
│ Creality K2 PLUS 3D Printer + Tools + Lab & Lapangan + Waktu (9 bulan) │
└──────────────────────────────────────────────────────────────────────────┘
```

---

## 3. ASUMSI DAN KONDISI EKSTERNAL

### 3.1 Asumsi Kritis (Critical Assumptions)

| Tahap | Asumsi | Risiko Jika Tidak Terpenuhi | Strategi Validasi |
|-------|--------|----------------------------|-------------------|
| **Input → Activities** | • Budget tersedia tepat waktu<br>• Sensor dapat dikirim sesuai schedule<br>• Tim peneliti komit penuh | • Delay project<br>• Cost overrun<br>• Quality compromise | • Pre-funding confirmation<br>• Supplier commitment letter<br>• Team work contract |
| **Activities → Output** | • Teknologi sensor bekerja di kondisi sungai<br>• Operator kooperatif<br>• Weather permissive untuk testing | • Prototype gagal<br>• Data insufficient<br>• Testing terhambat | • Proof of concept test<br>• Stakeholder engagement early<br>• Flexible testing schedule |
| **Output → Outcome** | • Operator adopt teknologi baru<br>• KSOP support implementasi<br>• Sistem reliable di long-term use | • Low adoption rate<br>• No policy support<br>• High maintenance cost | • User-centered design<br>• Continuous KSOP liaison<br>• Design for reliability |
| **Outcome → Impact** | • Regulasi mendukung scaling<br>• Funding tersedia untuk replikasi<br>• Demand dari operator lain tinggi | • Stuck di pilot level<br>• No scaling<br>• Limited impact | • Policy advocacy early<br>• Business model development<br>• Marketing & showcase |

### 3.2 Kondisi Eksternal (External Factors)

**Faktor Positif (Enabler):**
- Pemerintah mendorong inovasi teknologi maritim (program BESTARI SAINTEK)
- KSOP Samarinda proaktif dalam peningkatan keselamatan
- Ketersediaan teknologi sensor LiDAR yang mature dan affordable
- Awareness industri maritim terhadap safety semakin tinggi

**Faktor Negatif (Barrier):**
- Resistensi budaya operator yang sudah terbiasa navigasi konvensional
- Keterbatasan regulasi yang spesifik untuk teknologi sensor pada tugboat
- Ketergantungan pada supplier internasional untuk sensor
- Potensi vandalism atau theft pada peralatan mahal

**Mitigasi Faktor Negatif:**
- Change management approach dengan training dan demonstrasi manfaat
- Proactive policy dialogue dengan regulator
- Explore local assembly/integration untuk reduce dependency
- Security design (hidden installation, alarm system)

---

## 4. MONITORING, EVALUATION, AND LEARNING (MEL) FRAMEWORK

### 4.1 Monitoring Plan

| Level | Indikator | Metode Pengumpulan Data | Frekuensi | PIC |
|-------|-----------|-------------------------|-----------|-----|
| **Input** | • Budget utilization rate<br>• Material arrival on-time<br>• Team attendance | • Financial report<br>• Procurement log<br>• Attendance sheet | Monthly | Ketua Tim |
| **Activities** | • Milestone completion %<br>• Task on-schedule rate<br>• Issue occurrence | • Gantt chart tracking<br>• Project management tool<br>• Issue tracker | Weekly | Project Manager |
| **Output** | • Prototype functionality test<br>• Training completion rate<br>• Document completeness | • Lab test report<br>• Training log<br>• Document checklist | Per deliverable | Technical Lead |
| **Outcome** | • Adoption rate<br>• Incident reduction<br>• User satisfaction | • Deployment register<br>• KSOP report<br>• Survey | Quarterly | Field Coordinator |
| **Impact** | • Accident rate trend<br>• Policy changes<br>• Replication cases | • Statistical analysis<br>• Policy review<br>• Case documentation | Annually | Ketua Tim + KSOP |

### 4.2 Evaluation Timeline

| Jenis Evaluasi | Waktu | Tujuan | Metode |
|----------------|-------|--------|--------|
| **Formative Evaluation** | Mid-term (Bulan 5) | • Assess progress<br>• Identify bottlenecks<br>• Adjust strategy | • Team review meeting<br>• KSOP mid-term review<br>• Technical audit |
| **Summative Evaluation** | End of project (Bulan 9) | • Assess overall achievement<br>• Measure output indicators<br>• Lessons learned | • Final report analysis<br>• Stakeholder satisfaction survey<br>• Technical performance review |
| **Impact Evaluation** | Year 2-3 post-project | • Measure long-term impact<br>• Assess sustainability<br>• Document replication | • Longitudinal study<br>• Comparative analysis<br>• Case study documentation |

### 4.3 Learning and Adaptation

**Learning Questions:**
1. Apa faktor kunci kesuksesan adopsi teknologi oleh operator tradisional?
2. Bagaimana sistem performa dalam berbagai kondisi cuaca ekstrem?
3. Model bisnis seperti apa yang sustainable untuk scaling teknologi ini?
4. Apa pembelajaran untuk replikasi di sungai lain dengan karakteristik berbeda?

**Adaptation Mechanism:**
- Sprint retrospective setiap akhir fase untuk identify improvement
- Feedback loop dengan operator melalui monthly focus group discussion
- Technical review dengan expert external setiap 3 bulan
- Policy dialogue dengan KSOP untuk alignment regulasi

---

**KERANGKA LOGIS DAN TEORI PERUBAHAN INI MENGGAMBARKAN PATHWAY YANG JELAS DARI INPUT MENUJU IMPACT JANGKA PANJANG, DENGAN ASUMSI DAN MEKANISME MONITORING YANG ROBUST UNTUK MEMASTIKAN KEBERHASILAN DAN KEBERLANJUTAN PROGRAM**
