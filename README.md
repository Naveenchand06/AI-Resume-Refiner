# AI Resume Refiner

This Streamlit application uses Google's Gemini AI model to provide feedback on resumes. It allows users to upload a PDF or TXT file of their resume and receive an analysis focusing on content clarity, skills presentation, experience descriptions, and suggestions for improvement.

## Features

- **Resume Upload:** Accepts PDF and TXT resume files.
- **Job Role Targeting:** Allows users to specify the job role they're targeting for more tailored feedback.
- **AI-Powered Analysis:** Utilizes Google's Gemini AI to analyze the resume content.
- **Structured Feedback:** Provides clear, structured feedback with specific recommendations.
- **Streamlit Interface:** User-friendly web interface built with Streamlit.

## Prerequisites

- Python
- Google Gemini API Key (see instructions below)

## Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/Naveenchand06/AI-Resume-Refiner.git
    cd ai-resume-refiner
    ```

2.  **Create a virtual environment (recommended):**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Linux/macOS
    venv\Scripts\activate  # On Windows
    ```

3.  **Install dependencies:**

    ```bash
    pip install streamlit PyPDF2 python-dotenv google-generativeai
    ```

## Getting a Google Gemini API Key

1.  Go to the Google AI Studio website: [https://makersuite.google.com/app/apikey](https://makersuite.google.com/app/apikey)
2.  Sign in with your Google account.
3.  Create a new API key.
4.  Copy the API key to use in the next step.

## Configuration

1.  **Create a `.env` file:**

    Create a file named `.env` in the root directory of the project. This file will store your API key securely. **Make sure to add `.env` to your `.gitignore` file to prevent committing your API key to a public repository.**

2.  **Add your API key to the `.env` file:**

    ```
    GOOGLE_API_KEY="YOUR_GEMINI_API_KEY"
    ```

    Replace `YOUR_GEMINI_API_KEY` with the API key you obtained from Google AI Studio.

## Running the Application

1.  **Run the Streamlit app:**

    ```bash
    streamlit run app.py
    ```

    (Assuming your main script is named `app.py`)

2.  **Access the application:**

    Open your web browser and navigate to the URL displayed in the terminal (usually `http://localhost:8501`).

## Usage

1.  **Upload your resume:** Click the "Browse files" button to upload your resume file (PDF or TXT).
2.  **Enter the job role (optional):** Type the specific job role you are targeting in the text input field. This will help tailor the analysis to that specific role. If you leave it blank, the analysis will provide general feedback.
3.  **Click "Analyze Resume":** Press the "Analyze Resume" button to start the AI-powered analysis.
4.  **View the results:** The analysis results will be displayed below the button, providing feedback and recommendations for your resume.
