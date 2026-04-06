# VisaScope AI: Local ML Edition 🌍🛡️

VisaScope AI is a full-stack, privacy-focused visa status estimator. Unlike traditional AI apps that rely on external APIs (like Google Gemini or OpenAI), this version runs a **Local Machine Learning Engine** directly on your PC using Python and Scikit-learn.

## 🚀 Key Features
- **Local ML Engine**: Powered by a Random Forest Classifier trained on historical visa data.
- **Privacy First**: Zero external API calls for predictions. Your data stays on your machine.
- **Full-Stack Architecture**: React 19 Frontend, Node.js (Express) Backend, and Python ML Service.
- **Real-Time UI**: Instant feedback on approval probability, risk levels, and processing times.
- **Mock Auth**: A built-in local authentication system for a seamless offline experience.

---

## 🛠️ Tech Stack
- **Frontend**: React 19, Vite, Tailwind CSS, Lucide Icons, Recharts.
- **Backend**: Node.js, Express, TypeScript.
- **ML Engine**: Python 3, Scikit-learn, Pandas.
- **Communication**: Child Process spawning (Node.js to Python bridge).

---

## 📋 Prerequisites
Before running the project, ensure you have the following installed:
1. **Node.js** (v18 or higher)
2. **Python** (v3.10 or higher)
3. **pip** (Python package manager)

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/Abhiram1928/visacope.ai.git
cd visascope.ai
```

### 2. Install Node.js Dependencies
```bash
npm install
```

### 3. Install Python ML Libraries
```bash
pip install pandas scikit-learn
```

---

## 🏃 How to Run
To start both the frontend and the backend simultaneously, run:
```bash
npm run dev
```
The application will be available at: **`http://localhost:3000`**

---

## 🧠 How the ML Model Works
The core logic resides in `ml_model.py`. 
- **Algorithm**: Random Forest Classifier.
- **Features Analyzed**: Nationality, Destination, Visa Type, Monthly Income, and Travel History.
- **Preprocessing**: Uses `LabelEncoder` to transform categorical data into numerical features.
- **Inference**: When you submit the form, the Node.js server spawns a Python process, passes your data as JSON, and receives a structured prediction result.

---

## 📁 Project Structure
- `src/`: React frontend components and logic.
- `server.ts`: Express backend server and Python bridge.
- `ml_model.py`: The Python Machine Learning engine.
- `components/`: Reusable UI components (Layout, PredictionDisplay, etc.).
- `services/`: Frontend services for API communication.

---

## 🛡️ Privacy & Security
This project is designed to be **completely offline**. It does not require a Google Cloud account, Firebase setup, or any third-party API keys. Geolocation is handled via the browser's native API and OpenStreetMap (Nominatim).

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).

---
*Developed with 💙 for secure and private visa analysis.*
