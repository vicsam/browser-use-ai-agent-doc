# Browser-Use AI Agent Documentation

This is a personal documentation on Browser-Use AI Agent, compiling all the challenges I faced when running it locally.

## Overview
Browser-Use AI Agent is an AI-driven agent that takes control of your web browser, utilizing user-provided prompts to deliver desired results.

## Challenges and Solutions
### 1. Setting Up Browser-Use
**Official Documentation:** [Browser-Use GitHub Repository](https://github.com/browser-use/browser-use)

### 2. Virtual Environment Requirement for Python Package Installation
When setting up Browser-Use, it is recommended to use a virtual environment. To do so:
- Navigate to the project folder in your terminal.
- Run the virtual environment installation command.

**Issue:** If you face challenges running a virtual environment for Browser-Use, try installing the required packages without a virtual environment.
- **Alternative Solution:** Ensure you are using Python 3.11. You can download it here: [Python 3.11 Download](https://www.python.org/downloads/release/python-3110/).

### 3. Setting the Browser Path on Windows
By default, the code is set up with a MacOS-specific Chrome path. If you are on Windows, modify the path in the code as follows:
```python
CHROME_PATH = "C:\\Program Files\\Google\\Chrome\\Application\\chrome.exe"
CHROME_USER_DATA = "C:\\Users\\YourUsername\\AppData\\Local\\Google\\Chrome\\User Data"
```
Replace `YourUsername` with your actual Windows username.

### 4. Storing API Keys
To enhance security, store all API keys in a `.env` file instead of hardcoding them in your scripts.

### 5. Installing AI API Dependencies
When using an AI API, ensure that the required packages are installed.

#### AI21 API Setup
If using the AI21 API, install the following Python packages:
```bash
python -m pip install --upgrade pip setuptools wheel
pip install sentencepiece
pip install ai21
```

**Prerequisite:** Before installing these packages, you need to install **Visual C++ Build Tools** from [Microsoft Build Tools](https://visualstudio.microsoft.com/visual-cpp-build-tools/).

**Installation Steps:**
1. Choose the **Desktop development with C++** workload.
2. Under **Installation details**, ensure the following components are selected:
   - **MSVC v143 - VS 2022 C++ x64/x86 build tools** (or the version matching your Python installation).
   - **Windows 10 SDK** (or the SDK matching your Windows version).
   - **C++ CMake tools for Windows**.
   - **C++ AddressSanitizer** (optional but recommended for debugging).
3. After installing the Build Tools, proceed with the package installations listed above.

## Conclusion
This documentation summarizes the challenges I encountered while running Browser-Use AI Agent locally and the solutions I implemented. It serves as a reference for troubleshooting and optimizing the setup process.

