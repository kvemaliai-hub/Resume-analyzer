Features
Extract name
Extract email
Extract mobile numbers
Extract skills
Extract total experience
Extract college name
Extract degree
Extract designation
Extract company names
Installation
You can install this package using
pip install pyresparser
For NLP operations we use spacy and nltk. Install them using below commands:
# spaCy
python -m spacy download en_core_web_sm

# nltk
python -m nltk.downloader words
python -m nltk.downloader stopwords
Documentation
Official documentation is available at: https://www.omkarpathak.in/pyresparser/

Supported File Formats
PDF and DOCx files are supported on all Operating Systems
If you want to extract DOC files you can install textract for your OS (Linux, MacOS)
Note: You just have to install textract (and nothing else) and doc files will get parsed easily
Usage
Import it in your Python project
from pyresparser import ResumeParser
data = ResumeParser('/path/to/resume/file').get_extracted_data()
CLI
For running the resume extractor you can also use the cli provided

usage: pyresparser [-h] [-f FILE] [-d DIRECTORY] [-r REMOTEFILE]
                   [-re CUSTOM_REGEX] [-sf SKILLSFILE] [-e EXPORT_FORMAT]

optional arguments:
  -h, --help            show this help message and exit
  -f FILE, --file FILE  resume file to be extracted
  -d DIRECTORY, --directory DIRECTORY
                        directory containing all the resumes to be extracted
  -r REMOTEFILE, --remotefile REMOTEFILE
                        remote path for resume file to be extracted
  -re CUSTOM_REGEX, --custom-regex CUSTOM_REGEX
                        custom regex for parsing mobile numbers
  -sf SKILLSFILE, --skillsfile SKILLSFILE
                        custom skills CSV file against which skills are
                        searched for
  -e EXPORT_FORMAT, --export-format EXPORT_FORMAT
                        the information export format (json)
