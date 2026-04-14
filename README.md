# QuDrugGuard

> **Quantum-powered drug interaction checker**. Built for World Quantum Day 2026 by Team Quantum Five.

QuDrugGuard uses a hybrid Quantum SVM model to predict dangerous drug interactions. It intoduces a full multi-screen web app with secure authentication, a 120-drug database, automatic enzyme detection, a Gemini AI assistant, 100+ language translation support, and a personal check history dashboard.

---

## Features

- **Animated Landing Page** - dark-themed entry point with statistics and a _Get Started_ CTA
- **Secure Auth** - login and signup backed by bcrypt password hashing and a local SQLite database
- **Drug Category Browser** - 120 drugs across 12 categories, selectable as pill chips (no manual sliders)
- **Auto Enzyme Detection** - shared enzyme pathways are identified automatically; no user input required
- **Quantum SVM Prediction** - hybrid quantum circuit + classical SVM predicts interaction risk
- **Multi-Modal AI Scanner** - scan drug labels or pill images for automatic identification
- **Gemini AI Assistant** - ask questions about drug interactions in natural language
- **100+ Language Translation** - full app support for over 100 languages
- **Check History Dashboard** - per-user history with metric cards for total, dangerous, and safe checks

---

## Project Structure

```
QuDrugGuard_V2/
├── .streamlit/          
├── assets/              
├── app.py               
├── auth.py                
├── drug_db.py             
├── data.py               
├── quantum_circuit.py     
├── train.py              
├── run_all.py            
├── requirements.txt       
├── qudrug_model.pkl      
└── users.db              
```

---

## Setup & Running

### 1. Clone the repository

```bash
git clone https://github.com/thatarcticpenguin/QuDrugGuard.git
cd QuDrugGuard
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Verify auth module

```bash
python auth.py
# Expected: Signup OK, Login OK, Wrong password rejected
```

### 4. Verify drug database

```bash
python drug_db.py
# Expected: Total drugs: 120, 12 categories, correct enzyme checks
```

### 5. Train the model *(optional — pre-trained model included)*

```bash
python train.py
# Regenerates qudrug_model.pkl — takes 30–60 seconds
```

### 6. Run integration test

```bash
python run_all.py
# Expected: ALL CHECKS PASSED
```

### 7. Launch the app

```bash
streamlit run app.py
```

Open [http://localhost:8501](http://localhost:8501) in your browser. You'll land on the animated landing page. Navigate: **Get Started → Login/Signup → Drug Checker → History**.

---

## Tech Stack

| Layer | Technology |
|---|---|
| UI | Streamlit |
| Auth | bcrypt + SQLite |
| Drug data | Custom Python module (`drug_db.py`) |
| ML model | Quantum SVM (hybrid quantum-classical) |
| Quantum circuit | `quantum_circuit.py` |
| AI assistant | Google Gemini API |
| Translation | 100+ language support via translation API |
| Image scanning | Multi-modal AI scanner |

---

## Team

| Member | Role |
|---|---|
| **Sairam** | Team Lead · Quantum circuit integration |
| **Sabareesh** | Dataset integration |
| **Sreehas** | Model training |
| **Laasya** |  All screens + CSS |
| **Srujana** | Documentation · README |

---

*Built for World Quantum Day 2026.*

Click below thumbnail to watch demo video.
<a href="https://drive.google.com/file/d/1L7xyOYe8DhabOCoRm3uRLzgB0Bo6KzRH/preview">
<img width="1298" height="727" alt="Screenshot 2026-04-14 002751" src="https://github.com/user-attachments/assets/5ce3bfbd-e23f-49c4-996a-5b101f2a853c" />
</a>
