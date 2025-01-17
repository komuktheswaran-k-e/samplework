# komuktheswaran-k-e-wasserstoff-AiInternTask
# PDF Processing Pipeline

This project implements a dynamic pipeline that processes PDF documents from a specified folder, generating domain-specific summaries and keywords, and storing the results in a MongoDB database.

## Overview

The PDF Processing Pipeline performs the following key functions:
- **PDF Ingestion**: Reads and extracts text from multiple PDF documents.
- **Summarization**: Generates concise summaries based on the frequency of terms in the text.
- **Keyword Extraction**: Extracts relevant keywords using the RAKE (Rapid Automatic Keyword Extraction) algorithm.
- **Data Storage**: Stores the processed data, including document metadata, summaries, and keywords, in a MongoDB collection.

## System Requirements

- **Python**: Version 3.7 or higher
- **MongoDB**: Version 4.0 or higher (running locally or remotely)
- **Required Python Libraries**:
  - `pymongo`
  - `rake_nltk`
  - `memory-profiler`
  - `PyPDF2`

## Setup Instructions

1. **Install Python**: Ensure you have Python installed on your system. You can download it from [python.org](https://www.python.org/downloads/).

2. **Install MongoDB**: Follow the installation instructions on the [MongoDB website](https://docs.mongodb.com/manual/installation/) to set up MongoDB.

3. **Clone the Repository**:
   ```bash
   git clone https://github.com/komuktheswaran-k-e/komuktheswaran-k-e-wasserstoff-AiInternTask.git
   cd pdf-processing-pipeline
Install Required Libraries: Use pip to install the necessary libraries:

bash
Copy code
pip install pymongo rake_nltk memory-profiler PyPDF2
Update the Folder Path: In the main function of the script, update the folder_path variable to point to the directory containing your PDF files:

python
Copy code
folder_path = 'path_to_your_pdf_folder'  # Update this to your PDF folder path
Run the Script: Execute the script using Python:

bash
Copy code
python your_script_name.py
How It Works
PDF Ingestion: The pipeline scans the specified folder for PDF files. It reads each file and extracts text content using the PyPDF2 library.

Summarization: The extracted text is analyzed to create a summary. The script identifies important sentences based on the frequency of words, selecting the top sentences to include in the summary.

Keyword Extraction: After summarization, the script uses the RAKE algorithm to identify and extract domain-specific keywords from the text.

MongoDB Storage: Finally, the metadata, summary, and keywords are stored in a MongoDB database. Each document's information is stored as a new entry in the specified collection.

Performance Monitoring
The script also monitors its performance, logging execution time and peak memory usage for each PDF processed. This helps identify potential bottlenecks and optimize the processing pipeline.

Contributing
Feel free to submit issues or pull requests to improve the project. Contributions are always welcome!