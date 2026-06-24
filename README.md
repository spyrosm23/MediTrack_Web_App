# 🏥 MediTrack - Hospital Information System (Web Client)

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Web-lightgrey.svg)
![Firebase](https://img.shields.io/badge/firebase-Auth%20%7C%20Firestore%20%7C%20Storage-orange.svg)

**MediTrack** is a modern, real-time Hospital Information System (HIS) built to seamlessly connect hospital reception, doctors, and nursing staff. It features a futuristic dark-themed UI and relies on Firebase for real-time data synchronization.

📱 **Ecosystem Note:** This repository contains the **Web Application** (designed for Doctors and Reception/Admin). It works in tandem with the **MediTrack Android Application** (designed for Nursing staff on the floor). 
👉 **[View the Android Application Repository Here](https://github.com/spyrosm23/MediTrack)**

---

## 🚀 Key Features

The web client is divided into two main environments (Single Page Applications):

### 👨‍⚕️ 1. Doctor Dashboard (`dashboard.html`)
The secure workspace for attending physicians.
* **Authentication:** Secure login via Firebase Auth.
* **Live Vitals Monitoring:** Real-time tracking of patient vitals (Blood Pressure, Heart Rate). Includes a **Visual Alert System** that flashes if a patient's temperature exceeds 38°C.
* **Vitals History:** Chronological log of all past vital measurements and nursing clinical notes.
* **Digital Medical Orders (Tasks):** Doctors can dispatch medication or exam orders directly to the nurses' Android tablets in real-time.
* **Medical Records:** Dynamic retrieval and viewing of patient files and exam results (PDFs/Images) from Firebase Storage.
* **Patient Management:** Transfer patients between doctors or issue a formal "Discharge Request" to the reception.

### 🖥️ 2. Reception & Admin Panel (`reception.html`)
The control center of the clinic.
* **Patient Admissions:** Register new patients and assign them to attending doctors.
* **Discharge Management:** Review, approve, or reject discharge requests issued by doctors.
* **Archive & Readmission:** Automatically archive discharged patients and instantly restore them via a one-click "Readmission" feature.
* **Staff Management:** Add new doctors to the system. The panel uses a secondary Firebase Admin instance to automatically generate Auth credentials securely in the background.

---

## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3 (Custom Grid/Flexbox, Animations), Vanilla JavaScript (ES6+).
* **Backend as a Service (BaaS):** 
  * **Firebase Authentication:** For identity management.
  * **Cloud Firestore:** NoSQL database using `.onSnapshot()` listeners for real-time UI updates.
  * **Firebase Storage:** For medical file hosting.
* **UI/UX:** Google Fonts (Outfit), FontAwesome 6 (Icons).

---

## ⚙️ Setup & Installation

Since this is a client-side Vanilla JS application, no complex build tools or Node.js environments are required.

1. **Clone the repository:**
```bash
   git clone [https://github.com/YOUR_USERNAME/MediTrack-Web.git](https://github.com/YOUR_USERNAME/MediTrack-Web.git)
```
2. **Firebase Configuration:**
The code includes a configuration object. To run this on your own database, simply replace the firebaseConfig variables inside the <script> tags of both dashboard.html and reception.html.

3. **Run the App:**
It is highly recommended to serve the files using a local server (e.g., the Live Server extension in VS Code) to prevent CORS issues.

Open reception.html for the Admin/Reception panel.

Open dashboard.html for the Doctor workspace.



