# AI Health Checker (Offline)

## Overview

AI Health Checker is an interactive tool designed to provide users with a **quick assessment of potential diseases** based on the symptoms they describe. This offline application leverages a predefined database of diseases, symptoms, and recommendations to help users understand possible health conditions and urgent situations.

It is implemented as a **Jupyter Notebook application** with a modern and user-friendly interface. Users can type in their symptoms, and the system will return a **list of likely diseases**, along with a **match percentage** and **recommended actions**.

---

## Features

- **Symptom-Based Prediction**: The tool analyzes user-inputted symptoms against a curated disease database.
- **Urgent Symptom Detection**: Highlights critical conditions such as heart attack, shortness of breath, or chest pressure that require immediate medical attention.
- **Weighted Matching**: Uses keyword relevance and approximate string matching to generate a score for each possible disease.
- **Interactive GUI in Jupyter Notebook**: A clean, visually appealing layout with colored cards, progress bars, and recommendations.
- **Offline Functionality**: The tool works entirely offline using a local dataset, ensuring privacy and availability without an internet connection.
- **Expandable Symptom Recognition**: Recognizes different variations and synonyms of symptoms to improve prediction accuracy.

---

## How It Works (Theory)

1. **Input Processing**:
   - User enters a description of their symptoms into the interface.
   - The input is cleaned to remove punctuation and normalize text.

2. **Symptom Matching**:
   - Each disease in the database has a set of associated keywords (symptoms).
   - The system compares the user input with each disease keyword using exact and approximate matching techniques.
   - Synonyms and related symptom terms are optionally expanded for better matching.

3. **Scoring**:
   - For each disease, a **match score** is calculated based on the number of matched symptoms relative to the total symptoms for that disease.
   - Urgent symptoms (e.g., chest pain, shortness of breath) are flagged separately.

4. **Results Display**:
   - Diseases are ranked by match score and displayed in colored cards.
   - Urgent symptoms are highlighted at the top.
   - Each disease card shows:
     - Disease name
     - Match percentage
     - Recommended actions
     - A visual progress bar representing the score

---

## Intended Use

- **Educational Purpose**: Helps users understand potential diseases based on symptoms.
- **Quick Self-Assessment**: Provides immediate guidance on common conditions.
- **Not a Replacement for Medical Advice**: The tool is **not a diagnostic system** and should not replace consultation with a healthcare professional. Urgent or serious symptoms should always prompt medical attention.

---

## User Interaction

- Users enter their symptoms in plain language (e.g., "fever, throat pain, body ache").
- Click the **Check Now!** button to process the input.
- Results are displayed in an interactive and intuitive format with recommendations.
- Urgent health warnings are clearly indicated at the top.

---

## Technology Stack

- Python 3.x
- Jupyter Notebook
- `ipywidgets` for interactive GUI components
- HTML and CSS styling for results visualization
- Built-in libraries: `re` and `difflib` for text processing and matching

---

## Future Enhancements

- Expand disease and symptom database for broader coverage.
- Add AI/NLP-based symptom understanding for more accurate predictions.
- Provide multi-language support.
- Integrate with offline medical reference databases for updated recommendations.

---

**Disclaimer**: This project is for educational and informational purposes only. It **does not provide medical diagnosis**. Users should consult a qualified healthcare professional for any medical concerns or emergencies.
