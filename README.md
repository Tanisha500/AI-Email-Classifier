# AI Email Classifier using Hugging Face and Gmail API

A smart Streamlit-based AI application that connects to your Gmail account, fetches unread emails, and classifies them into categories (e.g., Important, Personal, Spam) using Hugging Face Transformers' zero-shot learning.


##  Features

-  Secure login using Gmail App Passwords
-  Fetch unread emails directly from Gmail (IMAP)
-  Classify emails using `facebook/bart-large-mnli` model
-  Display subject, predicted label, and confidence score
-  Clean, user-friendly Streamlit UI
-  Download classification results as a CSV file


##  Tech Stack

 Python : Core programming language           
 IMAP (imaplib) : Fetch unread Gmail messages    
 Hugging Face Transformers : Zero-shot classification model
 PyTorch : Backend for running Hugging Face models
 Streamlit : Interactive web UI frontend
 Pandas : Display classification table        



##  Screenshot

<img width="769" height="871" alt="image" src="https://github.com/user-attachments/assets/3a59a500-cc62-4ccb-8562-5dafac1672f3" />


## Screenshot of CSV file 

<img width="993" height="295" alt="image" src="https://github.com/user-attachments/assets/9bd08347-b36b-4fac-a41b-1aed70def258" />


##  Gmail Setup (One-time only)

1. **Enable IMAP** in Gmail:
   - Go to **Settings → See all settings → Forwarding and POP/IMAP**
   - Under "IMAP access", select **Enable IMAP**, then click **Save Changes**

2. **Generate App Password**:
   - Go to: [Google Account → Security → App Passwords]
   - Choose: `Mail` and your device (e.g., `Windows Computer`)
   - Copy the 16-character password (use this in the app)


## How It Works
1. Uses imaplib + Gmail App Password to fetch unread emails
2. Applies facebook/bart-large-mnli for zero-shot classification
3. Shows output in an interactive Streamlit UI with confidence scores


## Example Categories
The model automatically classifies into categories like:
- Important
- Personal
- Spam
- Newsletter
- Promotions

  
## Create a virtual environment 
python -m venv venv
venv\Scripts\activate   # for Windows


## Install dependencies
pip install --upgrade pip
pip install -r requirements.txt


## Run the App
streamlit run app.py

