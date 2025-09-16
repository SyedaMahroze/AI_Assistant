# AI_Assistant
📚 Educator Right Hand

An AI-powered assistant web application built using Flask, Python, and NLP.
It helps teachers or students by automatically generating:

✍️ Summary of a given story/text

❓ Questions from the text

✅ MCQs (fill in the blanks) from the text

🌐 Urdu Translation of the text

⚙️ Features

Summarization: Uses Hugging Face Transformers pipeline to summarize input text.

Question Generation: Uses pre-trained T5 model (valhalla/t5-base-qg-hl) to generate questions.

MCQs: Extracts nouns using NLTK and replaces them with blanks.

Translation to Urdu: Uses MarianMT model (Helsinki-NLP/opus-mt-en-ur).

📁 Project Structure
project/
│
├── app.py                # Flask app entry point
├── assistant.py          # NLP logic (summary, questions, mcqs, translation)
├── templates/
│   ├── index.html         # Home page (input form)
│   └── result.html        # Output results page
│
├── static/
│   └── css/
│       └── styles.css     # Styling for the app
│
└── README.md              # Project documentation

🖥️ Setup Instructions
1. Clone the repository
git clone https://github.com/your-username/educator-right-hand.git
cd educator-right-hand

2. Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate     # on Windows
# OR
source venv/bin/activate  # on Mac/Linux

3. Install dependencies
pip install flask nltk transformers sentencepiece


Also download required NLTK data:

import nltk
nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')

4. Run the application
python app.py


Then open your browser at:
http://127.0.0.1:5000/

💡 Usage

Enter your story or text in the text area.

Select what you want to generate:

Summary

Questions

MCQs

Click Process.

View your results on the result page.

📝 Technologies Used

Flask — backend web framework

NLTK — text tokenization & POS tagging

Hugging Face Transformers — for summarization, question generation, translation

HTML/CSS — frontend design

📌 Notes

The first model load might take some time (downloads models on first run).

Make sure you have a stable internet connection the first time you run it.

🤝 Contribution

Feel free to fork the repo, improve the design, add new features (like grammar correction or keyword extraction), and make pull requests!

📜 License

This project is licensed under the MIT License.
