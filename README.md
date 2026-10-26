# RadFlow AI: Diagnostic Radiology Operating System & Automated PACS Reporting Workstation

**RadFlow AI** is a professional, hospital-grade Radiology Information System (RIS) and Automated PACS Reporting platform built for radiologists, sonologists, and diagnostic imaging centers.

---

## 🌟 Key Architecture & Clinical Workflow Highlights

### 1. 🎙️ Automated Voice Note Parameter Recognition
- **Zero-Friction Dictation**: The doctor speaks into the microphone or uploads an audio voice note file (`.wav`, `.mp3`, `.m4a`).
- **Clause-Scoped Clinical NLP**: Intelligently isolates anatomical clauses to extract parameters without cross-organ contamination:
  - **Liver**: Measurements (e.g. `14.8 cm`), Echogenicity (`Grade-I / Grade-II fatty liver`, `normal`, `cirrhosis`).
  - **Gallbladder**: Calculi/stones (e.g. `8.5 mm`), Cholecystitis, Wall thickening, Lumen status.
  - **Kidneys**: Independent assessment of Right and Left Kidneys (e.g. `Right kidney 5.2 mm stone with mild hydronephrosis`, `Left kidney normal, no calculus`), or bilateral nephrolithiasis.
  - **Pelvic Viscera**: Uterine size, Fibroids (`3.2 cm intramural fibroid`), Ovaries, Prostate enlargement (BPH).
  - **Peritoneal Cavity**: Free fluid in pouch of Douglas vs. clear peritoneum.
  - **Diagnostic Impressions**: Automatically synthesized from all positive clinical findings.
- **Visual Parameter Update Card**: Displays a transparent table showing each parameter detected from the voice note, the spoken trigger, and the updated report value.

### 2. ✏️ Two-Way Synchronized Manual Parameter Editor (Doctor Direct Override)
- **Flexible Workstation Views**:
  - `⚡ Split View (Voice + Manual Editor)`: Work with voice dictation on top and fine-tune fields below.
  - `🎙️ Automated Voice Note Mode Only`: Clean, distraction-free voice-to-report interface.
  - `✏️ Manual Parameter Editor Only`: Direct form controls for fast manual adjustments.
- **Two-Way Synchronization**:
  - When a voice note is recorded or uploaded, it updates the manual input fields automatically.
  - When the doctor edits any field manually, the official report sheet on the right updates instantly in real time.

### 3. 📄 Authentic Official Diagnostic Letterhead & Publication-Grade PDF
- **Dual-Column Clinic Letterhead**: Clinic details on the left, Consultant Radiologist credentials and registration on the right.
- **Dynamic Patient Demographics Box**: Fully generalized for any patient in the queue (Patient Name, Age/Sex, Patient ID, Referring Doctor, Modality, Timestamp).
- **Centered Underlined Exam Title**: Standard radiology convention (e.g. `USG OF ABDOMEN AND PELVIS`).
- **Organ-by-Organ Findings with Bold Variables**: Prominently highlights measurements and pathology.
- **Underlined Impression & Digital Signature**: Formatted bulleted conclusions with doctor's digital verification hash.
- **1-Click PDF Download**: Generates vector-sharp PDFs using ReportLab.

### 4. 📋 Dynamic Intake & Smart Billing Engine
- Instant fee computation with automatic **+25% Emergency Surcharge**.
- Modality-based pricing:
  - *X-Ray*: ₹500
  - *Sonography (USG Abdomen & Pelvis)*: ₹1,200
  - *Obstetric USG*: ₹1,500
  - *CT Scan*: ₹2,500
  - *MRI*: ₹5,000
- Live printable billing invoice with 1-click transition to the reporting scribe.

### 5. 📄 Multimodal Referral Ingestion (OCR & Vision)
- Upload doctor prescriptions or external reports (PNG/JPG).
- Inbuilt AI extracts: Patient Name, Age, Gender, Referring Physician, Modality, Urgency, and Indication.
- 1-Click transfer to pre-fill Patient Intake & Scribe.

### 6. 📊 Department Inward/Outward Registry & Financial Ledger
- Real-time KPI counters: *Total Patients*, *Gross Revenue*, *Emergency Surcharges*, *Emergency Scans*.
- Master registry with status tracking (*"Draft Pending"*, *"Signed & Dispatched"*).
- 1-Click **Month-End Reconciliation CSV Export**.

---

## 🚀 How to Run Locally

### Run via PowerShell or Terminal:
```powershell
python -m streamlit run app.py
```

*(Or simply double-click [`run.bat`](file:///c:/Users/pranj/OneDrive/Desktop/genai%20micro/run.bat) in the project folder).*
