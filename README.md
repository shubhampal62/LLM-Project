# 🚀 Resume Enhancer AI

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![Groq](https://img.shields.io/badge/Groq-Powered-orange)

An intelligent system that enhances resumes to match job descriptions using state-of-the-art language models and Retrieval-Augmented Generation (RAG).

## ✨ Features

- **PDF Analysis**: Extract structured data from resumes and job descriptions
- **Resume Enhancement**: Tailor resumes to match specific job requirements
- **RAG Enhancement**: Leverage industry-specific knowledge to further optimize resumes
- **Comprehensive Evaluation**: Score resume-job matches using multiple criteria
- **Web Interface**: User-friendly application for resume uploads and enhancements

## 📋 Overview

This project automates the process of tailoring resumes to specific job descriptions. By analyzing both the job description and the candidate's resume, the system provides customized enhancements to better position the candidate for success. The system employs large language models (LLMs) and Retrieval-Augmented Generation (RAG) for more intelligent and contextually relevant enhancements.

## ⚙️ Architecture


### Key Components:
1. **PDF Analysis System**:
   - Extracts text from resume and job description PDFs
   - Structures data into JSON format
   - Identifies key skills and requirements

2. **Base Enhancement System (R1)**:
   - Aligns resume skills with job requirements
   - Highlights relevant work experience
   - Emphasizes matching projects and achievements

3. **RAG Enhancement System (R2)**:
   - Incorporates domain-specific knowledge
   - Applies industry best practices
   - Optimizes terminology and presentation

4. **Evaluation System**:
   - Skill matching assessment
   - Grammar and writing quality analysis
   - Overall resume-job alignment scoring

## 🛠️ Installation

```bash
# Clone the repository
git clone https://github.com/your-username/resume-enhancer.git
cd resume-enhancer

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Download language model
python -m spacy download en_core_web_sm
```

## 🔧 Configuration

Create a `.env` file in the root directory:

```
GROQ_API_KEY=your_groq_api_key_here
```

## 🚀 Usage

### Command Line Interface

```bash
python enhance_resume.py --resume path/to/resume.pdf --job path/to/job.pdf
```

### Web Interface

```bash
streamlit run app.py
```

Then open your browser and navigate to the URL displayed in the terminal (typically http://localhost:8501).

## 📊 Evaluation Results

Our evaluation on test pairs showed the following average scores:

### Llama-3.1-70B-Versatile
- Original Resume (R): 0.435
- Basic Enhanced (R1): 0.627
- RAG Enhanced (R2): **0.635**

### Llama-3.2-90B-Text-Preview
- Original Resume (R): 0.437
- Basic Enhanced (R1): 0.577
- RAG Enhanced (R2): 0.578

The **Llama-3.1-70B-Versatile model with RAG enhancement (R2)** achieved the best overall performance.

## 📝 Evaluation Criteria

- **Skill Matching**: How well the resume's skills align with job requirements
- **Grammar Quality**: Assessment of writing quality and professionalism
- **Content Alignment**: Overall semantic matching between resume and job description

## 🖥️ Frontend Application

The web interface provides an intuitive way for users to:
- Upload resume and job description PDFs
- View extracted information
- Access enhanced resume versions
- Download the optimized resume


## 🙏 Acknowledgements

- [Groq](https://groq.com) for providing their powerful LLM API
- [Sentence Transformers](https://www.sbert.net) for semantic text processing
- [Streamlit](https://streamlit.io) for the web interface framework
- [PyPDF2](https://pypdf2.readthedocs.io) for PDF processing capabilities
