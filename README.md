Voice-Based Attendance System (ESP – Final)

This project implements a voice-based attendance system using deep learning–based speaker verification. The system uses Resemblyzer for voice embeddings and includes an AASIST3 model folder (already present in the project).

📌 Important Notes (Read First)

This project only works properly with Python 3.10.x

Newer Python versions (e.g. 3.11 / 3.12) cause dependency installation failures

Some dependencies fail to install automatically, so manual installation is required

🐍 Python Version Requirement

Before doing anything else:

# Uninstall other Python versions if needed
# Install Python 3.10.x


Verify:

python --version
# Should output: Python 3.10.x

📦 Installation Steps (IMPORTANT ORDER)
1️⃣ Install requirements

First, try installing the requirements file:

pip install -r requirements.txt


Some packages may fail here — this is expected.

2️⃣ Install Resemblyzer without dependencies

Resemblyzer’s automatic dependency installation fails due to missing files, so install it without deps:

pip install resemblyzer --no-deps

3️⃣ Manually install required dependencies

Install the missing dependencies manually:

pip install numpy scipy torch matplotlib
pip install librosa==0.9.2
pip install webrtcvad-wheels


After this step, Resemblyzer should work correctly.

✅ Setup Status

At this point:

✅ Python environment is ready

✅ Resemblyzer is fully set up

✅ All required dependencies are installed manually

📁 AASIST3 Folder

The AASIST3 folder is already included inside the project

It exists as a downloaded model directory

❌ No need to reinstall or add it again

❌ No extra setup required for AASIST3

🗂 Project Structure (Simplified)
Voice-Based-Attendance (Flow Complete)/
│
├── app.py
├── config.py
├── requirements.txt
├── AASIST3/
│   └── (pre-downloaded model files)
├── __pycache__/

▶️ Running the Project

Make sure your Flask app is properly configured (FLASK_APP=app.py if required).

Then run:

flask run

⚠️ Common Issues & Fixes
❌ Resemblyzer install fails

✔️ Fix: Install with --no-deps and then manually install dependencies

❌ Librosa errors

✔️ Fix: Use exactly:

pip install librosa==0.9.2

❌ Python version issues

✔️ Fix: Downgrade to Python 3.10.x

📚 Final Notes

Do not upgrade Python once the environment is working

Follow the installation order exactly

This setup was tested after multiple failures and works reliably
