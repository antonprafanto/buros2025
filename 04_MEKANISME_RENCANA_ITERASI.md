# MEKANISME RENCANA ITERASI
## Pengembangan Sistem Sensor LiDAR Anti-Collision - Agile Development Approach

---

## 1. OVERVIEW ITERASI

Penelitian ini mengadopsi **Agile Development Methodology** dengan 6 sprint/iterasi utama yang memungkinkan **continuous improvement** berdasarkan feedback dan evaluasi di setiap fase. Setiap iterasi memiliki **deliverable** yang jelas dan **kriteria sukses** yang terukur.

### Prinsip Agile dalam Penelitian Ini:

1. **Iterative Progress**: Pengembangan bertahap dengan evaluasi berkala
2. **User-Centric**: Melibatkan operator tugboat sejak awal sebagai co-creator
3. **Fail Fast, Learn Fast**: Identifikasi masalah sedini mungkin untuk perbaikan cepat
4. **Flexible but Focused**: Adaptif terhadap feedback namun tetap pada tujuan utama
5. **Collaborative**: Kerja sama erat antara peneliti, KSOP, dan operator

---

## 2. TIMELINE ITERASI (9 BULAN)

```
BULAN:  1      2      3      4      5      6      7      8      9
        │      │      │      │      │      │      │      │      │
        ├──────┼──────┼──────┼──────┼──────┼──────┼──────┼──────┤
ITERASI:│  I1  │      │  I2  │      │  I3  │  I4  │      │  I5  │ I6
        │      │      │      │      │      │      │      │      │
FASE:   │ Persiapan  │  Development │ Test │ Field Trial│ Eval │Fin
        └──────┴──────┴──────┴──────┴──────┴──────┴──────┴──────┘

I1 = Iterasi 1: Desain dan Inisiasi
I2 = Iterasi 2: Prototype Awal
I3 = Iterasi 3: Testing & Kalibrasi
I4 = Iterasi 4: Uji Lapangan Fase 1
I5 = Iterasi 5: Evaluasi & Improvement
I6 = Iterasi 6: Finalisasi & Diseminasi
```

---

## 3. DETAIL SETIAP ITERASI

---

## ITERASI 1: DESAIN DAN INISIASI (Bulan 1-2)

### Sprint Goal
Membangun fondasi proyek yang solid melalui pemahaman mendalam kebutuhan pengguna, desain sistem yang tepat, dan pengadaan seluruh material.

### Aktivitas Detail

#### Minggu 1-2: Kick-off dan Alignment

| Hari | Aktivitas | Output | PIC |
|------|-----------|--------|-----|
| **Hari 1-2** | • Kick-off meeting dengan tim peneliti<br>• Pembagian roles & responsibilities<br>• Setup project management tools | • Team charter<br>• Gantt chart<br>• Communication protocol | Ketua Tim |
| **Hari 3-5** | • Meeting dengan KSOP Samarinda<br>• Presentasi proposal<br>• Diskusi ekspektasi dan target | • MoU draft<br>• Joint workplan<br>• Access permission letter | Liaison Officer |
| **Hari 6-10** | • Observasi lapangan ke pelabuhan<br>• Observasi operasional tugboat<br>• Dokumentasi foto/video kondisi existing | • Field observation report<br>• Photo/video documentation<br>• Baseline data | Tim Lapangan |

#### Minggu 3-4: User Research

| Aktivitas | Metode | Target | Output |
|-----------|--------|--------|--------|
| **Interview Operator** | Semi-structured interview | 10 nahkoda & awak | • Interview transcript<br>• Pain points list<br>• User needs document |
| **Survey Kebutuhan** | Questionnaire | 20 operator tugboat | • Survey result analysis<br>• Priority ranking needs |
| **Expert Consultation** | FGD dengan KSOP | 3 expert maritim | • Expert recommendations<br>• Safety standard requirements |

**Key Findings Expected:**
- Jarak deteksi minimal yang dibutuhkan operator
- Preferensi interface (visual vs audio alert)
- Kondisi operasional paling challenging (kabut, malam, arus kuat)
- Concern terhadap kompleksitas teknologi

#### Minggu 5-6: System Design

| Komponen | Aktivitas Desain | Tool | Output |
|----------|------------------|------|--------|
| **Hardware Architecture** | • Pemilihan sensor (TF03 vs TFA300-L)<br>• Skema wiring diagram<br>• Power system design | Fritzing, Eagle CAD | • Schematic diagram<br>• Bill of Materials (BoM)<br>• Power calculation |
| **Software Architecture** | • Flowchart algorithm<br>• Data structure design<br>• Communication protocol | Draw.io, Lucidchart | • Algorithm flowchart<br>• Software requirement spec<br>• API documentation |
| **User Interface** | • Display layout mockup<br>• Alert system design<br>• Color coding scheme | Figma, Sketch | • UI mockup<br>• User flow diagram<br>• Style guide |
| **Mounting System** | • Posisi optimal sensor<br>• Bracket design<br>• Waterproof casing spec | CAD software | • 3D model mounting<br>• Installation guide draft |

**Design Review Meeting:**
- Internal review dengan tim (Minggu 6, Hari 1-2)
- External review dengan KSOP (Minggu 6, Hari 3)
- Revisi berdasarkan feedback (Minggu 6, Hari 4-5)

#### Minggu 7-8: Procurement

| Item Category | Procurement Activity | Timeline | Risk Mitigation |
|---------------|---------------------|----------|-----------------|
| **Sensor LiDAR** | • Vendor selection<br>• Purchase order<br>• Shipping arrangement | Week 7 | • Multiple vendor option<br>• Pre-order confirmation<br>• Tracking system |
| **Electronic Components** | • Local sourcing (Tokopedia/Bukalapak)<br>• Quality verification<br>• Arrival confirmation | Week 7 | • Local availability check<br>• Backup supplier list |
| **Fabrication Parts** | • Casing fabrication order<br>• Mounting bracket workshop<br>• Quality control | Week 7-8 | • Local workshop partnership<br>• Prototype sample check |
| **Tools & Equipment** | • Soldering station<br>• Multimeter, oscilloscope<br>• Development kit | Week 7 | • Lab facility check<br>• Rental option if needed |

**Procurement Checklist:**
- [ ] TF03 LiDAR x2 - Delivered
- [ ] TFA300-L LiDAR x2 - Delivered
- [ ] Arduino Mega/RPi x4 - Delivered
- [ ] Display, LED, Buzzer x4 set - Delivered
- [ ] Casing & Bracket x4 set - Fabricated
- [ ] All electronic components - Verified
- [ ] Tools ready - Checked

### Deliverables (Iterasi 1)

| No | Deliverable | Format | Approval By |
|----|-------------|--------|-------------|
| **D1.1** | MoU dengan KSOP Samarinda | PDF, signed | Ketua Tim + KSOP |
| **D1.2** | User Requirement Document | PDF, 15-20 hal | Ketua Tim |
| **D1.3** | System Design Document | PDF, 25-30 hal | Technical Lead |
| **D1.4** | Bill of Materials (BoM) Complete | Excel spreadsheet | Procurement Officer |
| **D1.5** | Gantt Chart Project | MS Project / Excel | Project Manager |
| **D1.6** | All Materials Arrived & Verified | Checklist form | Logistic Officer |

### Success Criteria (Iterasi 1)

✅ **PASSED** jika:
- MoU ditandatangani oleh kedua pihak
- User requirement document approved oleh minimal 3 operator senior
- System design mendapat approval dari expert reviewer external
- 100% material arrived on-time dan verified kualitas
- Timeline Gantt chart realistic dan agreed by all team members

❌ **REVIEW NEEDED** jika:
- Material delay > 1 minggu → Activate backup supplier
- Design rejected by expert → Re-design cycle (max 1 week)
- Budget overrun > 10% → Re-negotiate scope atau seek additional funding

### Sprint Review & Retrospective (End of Iterasi 1)

**Sprint Review Meeting** (Akhir Minggu 8):
- Presentation deliverables kepada KSOP
- Demo mockup dan design kepada operator pilot
- Get approval untuk lanjut ke Iterasi 2

**Sprint Retrospective** (Internal team):
- What went well? (celebrate successes)
- What didn't go well? (identify issues)
- What can we improve? (action items untuk iterasi berikutnya)

---

## ITERASI 2: PENGEMBANGAN PROTOTYPE AWAL (Bulan 3-4)

### Sprint Goal
Membangun prototype versi 1.0 (MVP - Minimum Viable Product) yang fungsional untuk indoor testing.

### Aktivitas Detail

#### Minggu 1-2: Hardware Assembly

**Workstation Setup:**
- Dedicated lab space dengan AC (untuk komponen sensitif)
- ESD-safe workbench
- Proper lighting dan ventilation

| Hari | Assembly Task | Checklist | PIC |
|------|---------------|-----------|-----|
| **Day 1-3** | **Sensor Integration** | □ Unbox sensor & verify condition<br>□ Connect sensor ke power supply<br>□ Test basic functionality (power-on)<br>□ Verify UART/CAN communication | Hardware Engineer |
| **Day 4-6** | **Microcontroller Setup** | □ Install bootloader<br>□ Test I/O pins<br>□ Connect sensor to MCU via UART<br>□ Verify data reception | Embedded Engineer |
| **Day 7-10** | **Peripheral Integration** | □ Connect LCD display<br>□ Connect LED indicators<br>□ Connect buzzer/alarm<br>□ Install SD card module<br>□ Wiring organization | Hardware Team |
| **Day 11-14** | **Power System** | □ Power supply circuit<br>□ Battery backup system<br>□ Voltage regulation test<br>□ Power consumption measurement | Electronics Technician |

**Quality Control:**
- Setiap koneksi diverifikasi dengan multimeter (continuity test)
- Solder joints inspected dengan magnifying glass
- Cable management rapi dan labeled
- Photo documentation setiap tahap assembly

#### Minggu 3-4: Software Development

**Development Environment:**
- Arduino IDE / Python (Raspberry Pi)
- Version control: Git/GitHub
- Code review: Peer review setiap module

| Module | Fungsi | Language | Lines of Code (Est.) | Status Tracking |
|--------|--------|----------|----------------------|-----------------|
| **Data Acquisition** | Komunikasi dengan sensor via UART/CAN, parsing data frame | C/C++/Python | ~200 LOC | □ Dev □ Test □ Done |
| **Signal Processing** | Filtering noise, averaging, outlier detection | C/C++/Python | ~150 LOC | □ Dev □ Test □ Done |
| **Decision Logic** | Threshold comparison, zone classification, alert triggering | C/C++/Python | ~100 LOC | □ Dev □ Test □ Done |
| **Display Driver** | Render jarak, status, grafik pada LCD | C/C++/Python | ~180 LOC | □ Dev □ Test □ Done |
| **Alarm Controller** | Audio alert pattern (slow/fast/continuous beep) | C/C++ | ~80 LOC | □ Dev □ Test □ Done |
| **Data Logger** | Write data ke SD card dengan timestamp | C/C++/Python | ~120 LOC | □ Dev □ Test □ Done |
| **Main Program** | Integration all modules, state machine | C/C++/Python | ~150 LOC | □ Dev □ Test □ Done |

**Software Development Workflow:**
```
[Requirement] → [Design] → [Code] → [Unit Test] → [Code Review] → [Integration] → [System Test]
```

**Unit Testing:**
- Setiap module ditest secara isolated
- Mock data untuk simulate sensor input
- Edge case testing (nilai ekstrem, null, error)

**Code Quality Standards:**
- Commenting minimal 20% dari total LOC
- Function naming: snake_case (C) / camelCase (C++)
- Error handling: proper exception/error code
- Memory leak check (untuk embedded system)

#### Minggu 5-6: Indoor Testing

**Test Environment:**
- Lab dengan space minimal 20 meter (untuk test range sensor)
- Objek standar: papan kayu, karton, kain (berbagai reflektivitas)
- Lighting: natural light, dim light, dark room

**Test Cases:**

| Test ID | Test Case | Procedure | Expected Result | Pass/Fail |
|---------|-----------|-----------|-----------------|-----------|
| **TC-01** | Basic Detection | Tempatkan objek di depan sensor (5m, 10m, 20m, 50m, 100m, 150m) | Jarak terdeteksi dengan akurasi ±10cm | ☐ P ☐ F |
| **TC-02** | Blind Zone | Objek pada jarak <0.1m | Tidak ada false reading | ☐ P ☐ F |
| **TC-03** | Zone Classification | Objek pada zona aman (>100m), waspada (50-100m), bahaya (<50m) | LED/alarm sesuai zona | ☐ P ☐ F |
| **TC-04** | Response Time | Pindahkan objek masuk ke zona bahaya | Alert trigger dalam <0.1 detik | ☐ P ☐ F |
| **TC-05** | Display Functionality | Verifikasi tampilan jarak, status, grafik | Display clear dan readable | ☐ P ☐ F |
| **TC-06** | Audio Alert | Trigger setiap zona | Slow beep (waspada), fast beep (bahaya) | ☐ P ☐ F |
| **TC-07** | Data Logging | Operasikan sistem 1 jam | Data tersimpan di SD card, timestamp akurat | ☐ P ☐ F |
| **TC-08** | Power Consumption | Ukur arus saat operasional | <200mA @ 12V | ☐ P ☐ F |
| **TC-09** | Continuous Operation | Operasikan sistem 8 jam non-stop | Tidak ada hang/crash/overheating | ☐ P ☐ F |
| **TC-10** | Multi-reflectivity | Objek dengan reflectivity berbeda (90%, 50%, 10%) | Detection range sesuai spek sensor | ☐ P ☐ F |

**Bug Tracking:**
- Setiap bug dicatat di issue tracker (severity: Critical, High, Medium, Low)
- Critical & High bugs harus resolved sebelum lanjut iterasi berikutnya
- Medium & Low bugs masuk backlog untuk iterasi selanjutnya

#### Minggu 7-8: Integration & Optimization

**System Integration:**
- Gabungkan dual sensor (TF03 + TFA300-L) dengan sensor fusion algorithm
- Implement voting mechanism (jika data kedua sensor berbeda)
- Optimize algoritma untuk reduce false positive

**Performance Optimization:**
- Code optimization untuk reduce latency
- Memory optimization (important untuk embedded system)
- Power optimization untuk extend battery life

**Casing & Packaging:**
- Install semua komponen ke dalam waterproof casing
- Cable management dengan cable ties dan heat shrink
- Labeling input/output ports
- Final aesthetic touch (logo, label instruksi)

### Deliverables (Iterasi 2)

| No | Deliverable | Description | Verification |
|----|-------------|-------------|--------------|
| **D2.1** | Prototype Hardware v1.0 | 4 unit sistem assembled | Physical inspection |
| **D2.2** | Source Code & Firmware | Complete codebase dengan dokumentasi | Code review passed |
| **D2.3** | Indoor Test Report | Hasil semua test cases | All critical tests passed |
| **D2.4** | Bug List & Resolution | Documented bugs dan status | Critical bugs = 0 |
| **D2.5** | User Manual Draft v0.1 | Basic operation guide | Readability test |

### Success Criteria (Iterasi 2)

✅ **PASSED** jika:
- 4 unit prototype hardware fully assembled dan functioning
- Sensor dapat detect objek dengan akurasi ±10cm (sesuai spek)
- Response time ≤ 0.1 detik
- Display & alarm berfungsi dengan baik
- Data logging berfungsi tanpa error
- System dapat beroperasi kontinyu minimal 8 jam tanpa crash
- Zero critical bugs

❌ **NEEDS IMPROVEMENT** jika:
- Akurasi di luar range ±10cm → Re-calibration needed
- Response time > 0.1 detik → Algorithm optimization
- Crash/hang saat operasi → Debug & fix memory leak
- Critical bugs exist → Must resolve before next iteration

### Sprint Review & Retrospective

**Demo Session:**
- Live demonstration prototype kepada KSOP dan operator pilot
- Show detection capability, interface, alert system
- Collect feedback untuk improvement

**Retrospective:**
- Technical challenges encountered dan how we solved them
- Collaboration effectiveness (hardware-software team)
- Timeline adherence (on-schedule? delays?)

---

## ITERASI 3: TESTING DAN KALIBRASI (Bulan 5)

### Sprint Goal
Mencapai performa optimal sistem melalui kalibrasi presisi dan stress testing dalam berbagai kondisi.

### Aktivitas Detail

#### Minggu 1-2: Calibration Process

**Calibration Setup:**
- Outdoor space dengan jarak terukur akurat (menggunakan laser measuring tool)
- Target standar dengan reflectivity known (white board 90%, gray board 50%, black cloth 10%)
- Weather monitoring (suhu, kelembaban, intensitas cahaya)

**Calibration Procedure:**

| Step | Activity | Method | Data Recorded |
|------|----------|--------|---------------|
| **1. Distance Calibration** | Tempatkan target pada jarak 1m, 2m, 5m, 10m, 20m, 50m, 100m, 150m, 180m | 10 measurements per distance | • Actual distance<br>• Measured distance<br>• Error (cm)<br>• Standard deviation |
| **2. Reflectivity Test** | Test dengan objek 90%, 50%, 10% reflectivity pada berbagai jarak | 5 measurements per config | • Max detection range per reflectivity<br>• Accuracy degradation curve |
| **3. Angle Calibration** | Test objek dengan sudut kemiringan 0°, 15°, 30°, 45° terhadap sensor | 5 measurements per angle | • Detection success rate<br>• Accuracy per angle |
| **4. Ambient Light Test** | Test pada kondisi: full sunlight (100Klux), cloudy (50Klux), dusk (10Klux), night (0Klux) | 5 measurements per condition | • Detection range per condition<br>• False alarm rate |

**Calibration Result Analysis:**
- Plot grafik: Jarak Aktual vs Jarak Terukur → Hitung linear regression
- Hitung mean error dan standard deviation untuk setiap range
- Jika systematic error terdeteksi → Apply correction factor dalam software
- Document calibration certificate dengan hasil dan correction factor

#### Minggu 3: Stress Testing

**Stress Test Scenarios:**

| Test | Condition | Duration | Success Criteria | Result |
|------|-----------|----------|------------------|--------|
| **Durability Test** | Operasional kontinyu non-stop | 24 jam | No crash, no overheating (temp <60°C) | ☐ Pass ☐ Fail |
| **Temperature Stress** | Operasi pada suhu ekstrem (simulate dengan heat gun/AC) | 35°C, 15°C, masing-masing 2 jam | Detection accuracy maintained | ☐ Pass ☐ Fail |
| **Vibration Test** | Getaran simulate kondisi mesin tugboat | 2 jam di vibration platform | No component loosening, data stable | ☐ Pass ☐ Fail |
| **Rain/Water Spray** | Water spray test untuk casing | 30 menit spray test | IP67 verified, no water ingress | ☐ Pass ☐ Fail |
| **EMI Test** | Electromagnetic interference dari motor/generator | Dekatkan dengan motor/generator running | No false trigger, data stable | ☐ Pass ☐ Fail |
| **Power Fluctuation** | Voltage variance 10V-14V (simulate battery voltage drop) | 1 jam | System stable, auto shutdown jika <9V | ☐ Pass ☐ Fail |

**Failure Mode Analysis:**
- Document setiap failure yang terjadi
- Root cause analysis menggunakan 5-Why method
- Implement corrective action
- Re-test untuk verify fix

#### Minggu 4: Algorithm Optimization

**Optimization Goals:**
1. **Reduce False Positive Rate** dari baseline ~10% menjadi <5%
2. **Improve Response Time** dari 0.1s menjadi 0.05s (jika possible)
3. **Extend Battery Life** dengan power-saving mode

**Optimization Techniques:**

| Technique | Implementation | Expected Improvement |
|-----------|----------------|----------------------|
| **Moving Average Filter** | Window size 5-10 samples untuk smooth data | Reduce noise-induced false positive |
| **Kalman Filter** | Predict trajectory objek bergerak | Improve tracking stability |
| **Adaptive Threshold** | Threshold berubah berdasarkan kondisi ambient light | Reduce false alarm di kondisi ekstrem |
| **Sleep Mode** | MCU sleep saat tidak ada deteksi (zona aman) | Reduce power consumption 30-40% |
| **Sensor Fusion** | Weighted average dari TF03 dan TFA300-L | Improve accuracy dan reliability |

**A/B Testing:**
- Compare performa algoritma BEFORE vs AFTER optimization
- Use same test dataset (recorded sensor data dari stress test)
- Metric: False positive rate, response time, accuracy

### Deliverables (Iterasi 3)

| No | Deliverable | Content | Approval |
|----|-------------|---------|----------|
| **D3.1** | Calibration Certificate | Calibration data, correction factors, validity period | Technical Lead |
| **D3.2** | Stress Test Report | All test results, failure analysis, corrective actions | Quality Assurance |
| **D3.3** | Prototype v1.5 (Optimized) | Hardware + firmware updated dengan optimasi | Ketua Tim |
| **D3.4** | Performance Metrics Dashboard | Accuracy, response time, false positive rate, uptime | Data Analyst |

### Success Criteria (Iterasi 3)

✅ **PASSED** jika:
- Calibration error < 5% untuk range 1-100m
- All stress tests passed tanpa critical failure
- False positive rate < 5%
- Response time ≤ 0.1 detik (target: 0.05 detik)
- Battery life ≥ 10 jam operasional
- System reliability > 95%

🔄 **ITERATE** jika criteria belum tercapai:
- Extended calibration session
- Additional algorithm tuning
- Hardware modification jika diperlukan

---

## ITERASI 4: UJI COBA LAPANGAN FASE 1 (Bulan 6-7)

### Sprint Goal
Validasi performa sistem dalam kondisi operasional nyata di Sungai Mahakam dan mengumpulkan data lapangan untuk evaluasi.

### Pre-Field Preparation (Minggu 0)

**Site Preparation:**
- Site visit ke dermaga dan tugboat pilot
- Diskusi dengan nahkoda untuk jadwal instalasi
- Persiapan tools instalasi (drill, bracket, cable ties)
- Safety briefing untuk tim lapangan

**Pilot Tugboat Selection:**
| Tugboat | Spec | Route | Rationale |
|---------|------|-------|-----------|
| **Tugboat A** | 500 HP, 25m, pushing 2 barges | Samarinda - Tenggarong (50 km daily) | High traffic route, representative operational condition |
| **Tugboat B** | 300 HP, 18m, pushing 1 barge | Samarinda - Loa Janan (30 km daily) | Smaller vessel, narrow river section, challenging navigation |

#### Minggu 1: Installation & Commission

**Installation Process (per tugboat: 2 hari)**

| Day | Time | Activity | Team |
|-----|------|----------|------|
| **Day 1 AM** | 08:00-12:00 | • Survey posisi mounting optimal<br>• Mark drilling points<br>• Pre-fit bracket | Hardware Team (3 orang) |
| **Day 1 PM** | 13:00-17:00 | • Drilling & mounting bracket<br>• Install sensor pada bracket<br>• Cable routing dari bow ke wheelhouse | Hardware Team |
| **Day 2 AM** | 08:00-12:00 | • Install display di wheelhouse<br>• Electrical connection<br>• Power system integration dengan tugboat power | Electrical Team (2 orang) |
| **Day 2 PM** | 13:00-17:00 | • System commissioning test<br>• Calibration on-site<br>• Operator training basic<br>• Acceptance sign-off | Full Team + Nahkoda |

**Installation Checklist (per tugboat):**
- [ ] Sensor mounted securely (torque checked)
- [ ] Sensor aligned properly (FOV clear, no obstruction)
- [ ] Cable routing neat dan protected (no sharp bend)
- [ ] Display visible dari posisi nahkoda
- [ ] Power connection stable (fuse installed)
- [ ] System power-on successful
- [ ] Detection test successful (test dengan objek known-distance)
- [ ] Data logging aktif
- [ ] Operator briefed dan comfortable dengan sistem
- [ ] Emergency contact number provided (24/7 hotline)

#### Minggu 2-5: Field Operation & Monitoring

**Daily Operational Monitoring:**

**Week 2 (Intensive Monitoring):**
- Tim on-site setiap hari (naik tugboat bersama operator)
- Real-time observation performa sistem
- Interview operator setiap end-of-day
- Daily log: deteksi events, false alarm, system issue

**Week 3-4 (Semi-Intensive Monitoring):**
- Tim on-site 3x per minggu
- Remote monitoring via data log download weekly
- Phone check-in dengan operator setiap hari
- Weekly meeting untuk review performa

**Week 5 (Remote Monitoring):**
- Tim hanya site visit 1x untuk maintenance dan data download
- Operator report anomaly via WhatsApp group
- Focus group discussion dengan operator mid-week

**Data Collection:**

| Data Type | Collection Method | Frequency | Storage |
|-----------|------------------|-----------|---------|
| **Automatic Log Data** | SD card logging (timestamp, distance, zone, alarm status) | Kontinyu (setiap deteksi) | SD card (downloaded weekly) |
| **Operator Log** | Manual logbook (incident, false alarm, system issue) | Daily | Paper logbook |
| **Interview Data** | Semi-structured interview | Weekly | Audio recording + transcript |
| **Video Documentation** | GoPro recording operasional (sample) | 2-3 trip per week | Video file |
| **Environmental Data** | Weather condition, river condition | Daily | Weather log form |

**Key Metrics Tracked:**

| Metric | Definition | Target | Tracking Tool |
|--------|------------|--------|---------------|
| **Detection Events** | Jumlah objek/kapal terdeteksi per trip | N/A (baseline data) | Auto log |
| **True Positive** | Deteksi benar (confirmed by operator) | >90% | Operator log |
| **False Positive** | Alarm palsu (tidak ada objek) | <5% | Operator log |
| **False Negative** | Missed detection (ada objek tapi tidak terdeteksi) | <2% | Operator observation |
| **System Uptime** | Persentase waktu sistem operational | >95% | Auto log |
| **Response Time** | Waktu dari deteksi hingga alarm | <0.1 detik | Auto log analysis |
| **User Satisfaction** | Operator rating (1-10 scale) | >7 | Weekly survey |

#### Minggu 6-7: Data Analysis & Documentation

**Data Processing:**
1. **Data Cleaning**: Remove corrupt data, outliers, incomplete logs
2. **Statistical Analysis**:
   - Descriptive statistics (mean, median, std dev) untuk detection distance
   - Detection success rate per kondisi (day/night, weather)
   - False alarm rate calculation
3. **Visualization**:
   - Histogram distribusi jarak deteksi
   - Time series plot system uptime
   - Heatmap false alarm by time-of-day
4. **Qualitative Analysis**:
   - Thematic analysis dari interview transcript
   - Operator feedback categorization

**Field Test Report Content:**
1. Executive Summary
2. Test Methodology
3. Quantitative Results (dengan grafik dan tabel)
4. Qualitative Findings (operator feedback)
5. Issues Encountered & Resolution
6. Lessons Learned
7. Recommendations for Improvement

### Deliverables (Iterasi 4)

| No | Deliverable | Format | Pages |
|----|-------------|--------|-------|
| **D4.1** | Field Test Report | PDF | 40-50 hal |
| **D4.2** | Data Log (Raw Data) | CSV files | N/A |
| **D4.3** | Interview Transcripts | PDF/Word | 15-20 hal |
| **D4.4** | Video Documentation | MP4 files | 2-3 jam total |
| **D4.5** | Issue Tracker & Resolution Log | Excel | N/A |
| **D4.6** | Operator Feedback Summary | PDF | 5-7 hal |

### Success Criteria (Iterasi 4)

✅ **PASSED** jika:
- System uptime > 95% selama periode field test
- True positive rate > 90%
- False positive rate < 5%
- Operator satisfaction score > 7/10
- Zero critical system failure yang membahayakan keselamatan
- Minimal 100 jam operational data terkumpul
- Minimal 50 detection events recorded

⚠️ **NEEDS IMPROVEMENT** jika:
- False positive rate 5-10% → Algorithm tuning needed
- User satisfaction 5-7 → Interface/usability improvement needed
- System uptime 85-95% → Reliability improvement needed

❌ **MAJOR REDESIGN NEEDED** jika:
- False positive rate > 10% → Back to algorithm development
- User satisfaction < 5 → Major UX/UI redesign
- System uptime < 85% → Hardware reliability issue, need rework

---

## ITERASI 5: EVALUASI DAN IMPROVEMENT (Bulan 8)

### Sprint Goal
Menganalisis hasil field test, mengimplementasikan improvement, dan memvalidasi bahwa sistem telah mencapai performa final yang optimal.

### Aktivitas Detail

#### Minggu 1-2: Comprehensive Evaluation

**Evaluation Workshop** (2 hari intensive):
- Peserta: Tim peneliti, KSOP, operator pilot, expert external
- Format: Presentation hasil field test + FGD

**Agenda:**
| Session | Topic | Method | Output |
|---------|-------|--------|--------|
| **Session 1** | Quantitative Results Presentation | Presentation + Q&A | Validated data interpretation |
| **Session 2** | Operator Experience Sharing | FGD (operator sharing pengalaman) | Deep insights user experience |
| **Session 3** | Technical Issues Deep Dive | Root cause analysis | Priority issue list |
| **Session 4** | Brainstorming Improvement | Design thinking workshop | Improvement ideas list |
| **Session 5** | Prioritization & Roadmap | MoSCoW method (Must/Should/Could/Won't) | Improvement roadmap |

**Gap Analysis:**

| Aspect | Target | Actual (Field Test) | Gap | Root Cause | Improvement Action |
|--------|--------|---------------------|-----|------------|-------------------|
| Accuracy | ±10cm | ±8cm | ✅ Exceed | - | Maintain |
| False Positive | <5% | 7% | ❌ -2% | Rain droplets on sensor lens | Add auto-wiper or hydrophobic coating |
| Response Time | <0.1s | 0.08s | ✅ Exceed | - | Maintain |
| User Satisfaction | >7/10 | 7.5/10 | ✅ Pass | Display too bright at night | Add auto-brightness adjustment |
| Battery Life | >10 jam | 9 jam | ❌ -1 jam | Continuous high-brightness display | Implement sleep mode & dim display when no alert |
| System Uptime | >95% | 96% | ✅ Exceed | - | Maintain |

#### Minggu 3: Implementation of Improvements

**Improvement Tasks:**

| Priority | Improvement | Implementation | Effort (days) | PIC |
|----------|-------------|----------------|---------------|-----|
| **MUST** | Add auto-brightness untuk display | PWM-based brightness control via ambient light sensor | 2 days | Software Dev |
| **MUST** | Implement power-saving mode | MCU sleep when zona aman (>100m), wake every 1s to scan | 3 days | Software Dev |
| **MUST** | Hydrophobic coating pada sensor lens | Apply nano-coating solution | 1 day | Hardware Tech |
| **SHOULD** | Improve alarm logic (graduated warning) | Change: continuous beep only if <30m, intermittent if 30-50m | 1 day | Software Dev |
| **SHOULD** | Add "mute" button untuk false alarm | Physical button untuk temporary mute (5 min), automatic unmute | 2 days | Hardware + Software |
| **COULD** | Add Bluetooth connection untuk smartphone app | Bluetooth module + basic Android app untuk monitoring | 5 days | (Future work) |

**Implementation & Testing:**
- Implement improvements pada 1 unit prototype dulu
- Lab testing untuk verify improvement effectiveness
- Jika successful, replicate ke 3 unit lainnya
- Mini field test (1 minggu) untuk validation

#### Minggu 4: Re-Testing & Validation

**Validation Test:**
- Install improved prototype v2.0 pada tugboat pilot
- 1 minggu intensive field test
- Focus: verify bahwa improvement resolved identified issues

**Comparative Analysis:**

| Metric | Before Improvement | After Improvement | Status |
|--------|-------------------|-------------------|--------|
| False Positive Rate | 7% | 4% | ✅ Improved |
| User Satisfaction | 7.5/10 | 8.5/10 | ✅ Improved |
| Battery Life | 9 jam | 11 jam | ✅ Improved |
| Display Usability (night) | 6/10 | 9/10 | ✅ Improved |

**Final Acceptance:**
- Jika all improvements validated successful → Proceed to Iterasi 6
- Jika still ada issues → Additional mini-iteration (extend 1 minggu)

### Deliverables (Iterasi 5)

| No | Deliverable | Content |
|----|-------------|---------|
| **D5.1** | Evaluation Report | Comprehensive analysis field test, gap analysis, improvement roadmap |
| **D5.2** | Prototype v2.0 (Final) | 4 unit sistem dengan all improvements implemented |
| **D5.3** | Improvement Validation Report | Comparative before-after analysis |
| **D5.4** | Updated Source Code | Firmware final version dengan all improvements |

### Success Criteria (Iterasi 5)

✅ **READY FOR FINALIZATION** jika:
- False positive rate < 5%
- User satisfaction > 8/10
- Battery life > 10 jam
- All "MUST" improvements implemented dan validated
- Zero critical bugs remaining

---

## ITERASI 6: FINALISASI DAN DISEMINASI (Bulan 9)

### Sprint Goal
Menyelesaikan seluruh dokumentasi, melakukan pelatihan massal, publikasi hasil penelitian, dan handover sistem kepada stakeholders.

### Aktivitas Detail

#### Minggu 1-2: Documentation Finalization

**Documentation Package:**

| Document | Purpose | Target Audience | Pages | Language |
|----------|---------|-----------------|-------|----------|
| **Installation Manual** | Guide instalasi step-by-step | Teknisi | 15 hal | Bahasa Indonesia |
| **User Manual** | Operasional daily use | Nahkoda & Operator | 20 hal | Bahasa Indonesia |
| **Maintenance Guide** | Troubleshooting & maintenance | Teknisi & Operator | 12 hal | Bahasa Indonesia |
| **Technical Specification** | Spec detail hardware/software | Engineer & Procurement | 10 hal | Bahasa Indonesia/English |
| **Training Module** | Material pelatihan operator | Trainer & Operator | 25 hal | Bahasa Indonesia |
| **Research Report (Final)** | Comprehensive research report | Funder (BESTARI SAINTEK) | 60 hal | Bahasa Indonesia |

**Document Review Process:**
- Internal review by team (proofreading, technical accuracy)
- External review by KSOP (regulatory compliance, clarity)
- Operator review (1-2 operator pilot) untuk user manual (readability test)
- Revisi berdasarkan feedback
- Final approval dan printing

**Translation (jika diperlukan):**
- Technical spec translated ke English untuk potential international interest
- Use professional technical translator
- Technical review by bilingual engineer

#### Minggu 3: Mass Training Program

**Training Workshop Design:**
- **Duration**: 2 hari (16 jam total)
- **Participants**: 20 operator tugboat (nahkoda + awak)
- **Venue**: Ruang pelatihan KSOP Samarinda atau aula institusi peneliti
- **Format**: 40% teori, 60% praktik

**Training Curriculum:**

| Day | Time | Module | Method | Duration |
|-----|------|--------|--------|----------|
| **Day 1 AM** | 08:00-09:00 | Opening & Ice Breaking | Presentation | 1 jam |
|  | 09:00-10:30 | Modul 1: Pengenalan Teknologi LiDAR & Prinsip Kerja | Lecture + Video | 1.5 jam |
|  | 10:30-12:00 | Modul 2: Arsitektur Sistem Anti-Collision | Lecture + Demo | 1.5 jam |
| **Day 1 PM** | 13:00-15:00 | Modul 3: Operasional System (Power On, Interface, Interpretasi Data) | Hands-on practice | 2 jam |
|  | 15:00-17:00 | Modul 4: Zona Bahaya & Prosedur Respons | Case study + Simulation | 2 jam |
| **Day 2 AM** | 08:00-10:00 | Modul 5: Troubleshooting Dasar & Maintenance | Hands-on practice | 2 jam |
|  | 10:00-12:00 | Modul 6: Praktik Langsung di Tugboat (Site Visit) | Field practice | 2 jam |
| **Day 2 PM** | 13:00-15:00 | Modul 7: Studi Kasus & Best Practices | Group discussion | 2 jam |
|  | 15:00-16:30 | Post-Test & Evaluation | Written test | 1.5 jam |
|  | 16:30-17:00 | Sertifikasi & Closing | Certification ceremony | 0.5 jam |

**Training Materials:**
- Slide presentation (PPT)
- Video tutorial operasional
- Printed handbook untuk setiap peserta
- Prototype untuk hands-on practice (4 unit, ratio 1:5 peserta)

**Training Evaluation:**
- Pre-test (sebelum training) untuk baseline knowledge
- Post-test (akhir training) untuk measure learning outcome
- Target: Post-test score minimal 80/100 untuk mendapat sertifikat
- Training satisfaction survey

**Certification:**
- Sertifikat resmi untuk operator yang lulus post-test
- Ditandatangani oleh: Ketua Tim Peneliti + Kepala KSOP Samarinda
- Berlaku sebagai bukti kompetensi operator

#### Minggu 4: Publication & Dissemination

**Scientific Publication:**

| Publication Type | Target Venue | Timeline | Status Tracking |
|------------------|--------------|----------|-----------------|
| **Journal Article** | Jurnal Nasional Terakreditasi (Sinta 2/3)<br>Contoh: Jurnal Teknik ITS, Jurnal Elektronika dan Telekomunikasi | Submit: Week 4<br>Expected acceptance: 3-6 bulan | □ Draft □ Submit □ Review □ Accept |
| **Conference Paper** | International Conference on Maritime Technology<br>atau: Seminar Nasional Teknik Elektro | Submit: Week 4<br>Presentation: 6-12 bulan | □ Draft □ Submit □ Accept □ Present |
| **Research Report** | Laporan akhir untuk BESTARI SAINTEK | Submit: Week 4 | □ Draft □ Final □ Submit |

**Paper Writing (dilakukan paralel sejak Iterasi 5):**
- **Title**: "Pengembangan Sistem Sensor LiDAR Anti-Collision untuk Meningkatkan Keselamatan Navigasi Tugboat di Sungai Mahakam Samarinda"
- **Abstract**: 200-300 kata (Bahasa Indonesia + English)
- **Keywords**: LiDAR, anti-collision, tugboat, Sungai Mahakam, keselamatan maritim
- **Structure**: Introduction, Literature Review, Method, Results, Discussion, Conclusion
- **Length**: 6000-8000 words (jurnal), 3000-4000 words (conference)

**Stakeholder Seminar:**
- **Date**: Akhir Minggu 4
- **Venue**: Auditorium institusi peneliti atau KSOP
- **Participants**: KSOP, operator tugboat, industri maritim, media, akademisi, mahasiswa
- **Format**:
  - Presentation hasil penelitian (45 menit)
  - Technology showcase & demo (30 menit)
  - Panel discussion (45 menit)
  - Networking session
- **Output**:
  - Media coverage (press release, news article)
  - Recommendation letter dari KSOP untuk implementasi lanjutan
  - Potential business partnership inquiries

**Handover Ceremony:**
- Serah terima 4 unit prototype kepada KSOP Samarinda
- Formal ceremony dengan Berita Acara Serah Terima (BAST)
- Commit KSOP untuk sustainability (maintenance, deployment ke tugboat lain)
- Photo session & documentation

### Deliverables (Iterasi 6)

| No | Deliverable | Recipient | Format |
|----|-------------|-----------|--------|
| **D6.1** | Complete Documentation Package (6 documents) | KSOP + Operator | Printed + PDF |
| **D6.2** | 4 Unit Prototype Final | KSOP Samarinda | Hardware + Instalation |
| **D6.3** | Training Certificate (20 pcs) | Trained operators | Printed certificate |
| **D6.4** | Training Report | BESTARI SAINTEK | PDF |
| **D6.5** | Journal/Conference Paper (submitted) | Journal/Conference | PDF |
| **D6.6** | Final Research Report | BESTARI SAINTEK | PDF + Hardcover |
| **D6.7** | KSOP Recommendation Letter | Team Peneliti | Official letter |

### Success Criteria (Iterasi 6)

✅ **PROJECT COMPLETE** jika:
- All documentation completed dan approved
- 20 operator trained dengan post-test score >80/100
- 4 unit prototype handed over to KSOP dengan BAST
- Journal paper submitted (accepted: bonus)
- Final report submitted to BESTARI SAINTEK
- KSOP recommendation letter obtained
- Stakeholder seminar executed successfully

---

## 4. MONITORING & CONTROL MECHANISM

### 4.1 Project Tracking Tools

| Tool | Purpose | Update Frequency | Owner |
|------|---------|------------------|-------|
| **Gantt Chart** | Timeline tracking, milestone management | Weekly | Project Manager |
| **Issue Tracker** | Bug tracking, task assignment | Daily | All team members |
| **Sprint Board** | Visual task progress (To Do, In Progress, Done) | Daily | Scrum Master |
| **Budget Tracker** | Financial monitoring | Bi-weekly | Financial Officer |
| **Risk Register** | Risk identification & mitigation | Bi-weekly | Risk Manager (Ketua Tim) |

### 4.2 Communication Protocol

**Regular Meetings:**
| Meeting | Frequency | Duration | Participants | Agenda |
|---------|-----------|----------|--------------|--------|
| **Daily Stand-up** | Daily (Senin-Jumat) | 15 menit | Core team | Yesterday, Today, Blockers |
| **Sprint Review** | End of each iteration | 2 jam | Team + KSOP + Operator pilot | Demo, Feedback, Approval |
| **Sprint Retrospective** | End of each iteration | 1 jam | Internal team only | What went well, What to improve |
| **Stakeholder Meeting** | Monthly | 1 jam | Team + KSOP + Funder (optional) | Progress update, Issues, Next steps |

**Communication Channels:**
- WhatsApp Group (quick communication, daily updates)
- Email (formal communication, document sharing)
- Video Conference (remote meeting jika diperlukan)
- Project Management Software (Trello/Asana/Notion)

### 4.3 Risk Management

**Risk Monitoring:**
- Review risk register setiap 2 minggu
- Identify new risks yang muncul
- Update mitigation strategy based on effectiveness

**Escalation Protocol:**
| Issue Severity | Definition | Response Time | Escalation To |
|----------------|------------|---------------|---------------|
| **Critical** | Project blocker, cannot proceed | Immediate (< 4 jam) | Ketua Tim + KSOP |
| **High** | Major delay atau quality impact | Same day (< 24 jam) | Ketua Tim |
| **Medium** | Moderate impact, workaround available | 2-3 days | Project Manager |
| **Low** | Minor inconvenience | 1 week | Team discussion |

---

## 5. LESSONS LEARNED & CONTINUOUS IMPROVEMENT

### 5.1 Knowledge Management

**Documentation:**
- Setiap iterasi: tulis "Lessons Learned" document
- Include: What worked well, What didn't, Recommendations
- Store di shared repository (Google Drive/GitHub)

**Knowledge Sharing:**
- Monthly knowledge sharing session internal team
- Brown bag lunch: informal sharing pengalaman
- Blog post atau artikel popular untuk disseminasi ke public

### 5.2 Continuous Improvement Mindset

**Kaizen Approach:**
- Tidak ada iterasi yang perfect
- Selalu ada room for improvement
- Encourage team members untuk suggest improvements
- Implement quick wins immediately

**Metrics-Driven:**
- Track velocity (tasks completed per week)
- Monitor quality metrics (bug rate, rework percentage)
- Analyze trend: improving or degrading?
- Data-driven decision making

---

## 6. POST-PROJECT SUSTAINABILITY PLAN

### Beyond Iterasi 6

**Short-term (3-6 bulan after project end):**
- Follow-up survey dengan operator yang telah dilatih
- Maintenance visit ke tugboat yang equipped dengan sistem
- Collect long-term performance data
- Address any issues yang muncul post-deployment

**Medium-term (6-12 bulan):**
- Phase 2 deployment: tambahan 5-10 tugboat
- Seek funding untuk scaling (CSR, government program, commercialization)
- Product improvement based on long-term feedback
- Develop local supply chain untuk spare parts

**Long-term (1-3 tahun):**
- Spin-off company atau licensing kepada maritime tech vendor
- Replication di sungai-sungai lain (Kapuas, Barito, Musi)
- Policy advocacy untuk mandatory anti-collision system
- Integration dengan AIS (Automatic Identification System) maritim

---

**MEKANISME RENCANA ITERASI INI DIRANCANG DENGAN FLEKSIBILITAS UNTUK BERADAPTASI TERHADAP KONDISI LAPANGAN, SAMBIL TETAP MENJAGA FOKUS PADA TUJUAN AKHIR: SISTEM SENSOR ANTI-COLLISION YANG FUNGSIONAL, RELIABLE, DAN DIADOPSI OLEH OPERATOR TUGBOAT**

**"FAIL FAST, LEARN FAST, IMPROVE CONTINUOUSLY"**
