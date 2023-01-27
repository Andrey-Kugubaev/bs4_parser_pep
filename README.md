# Static Web Parsing Project

---
![python](https://img.shields.io/badge/Python-3.9-green)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4.9.3-green)
![Regex](https://img.shields.io/badge/Regex-grey)
![flake8](https://img.shields.io/badge/flake8-4.0.1-green)
---
## Contents:
- [Introduction](#introduction)
- [First parser. What's new?](#first-parser-what's-new?)
- [Second parser. Python versions](#second-parser-python-versions)
- [Third parser. Downloading files](#third-parser-downloading-files)
- [Fourth parser. Parsing PEP documents](#fourth-parser-parsing-pep-documents)
- [Instruction to start](#instruction-to-start)

---
### <anchor>Introduction</anchor>
The project to write static web page parsers using python library ___BeautifulSoup___, _regular expressions (__regex__)_,
The project implements parsers for searching for new information, collecting information about Python versions, downloading an archive with documentation for the latest version of Python,
comparing and counting versions _PEP (Python Enhancement Proposals)_

----
### <anchor>First parser. What's new?</anchor>
The parser collects links to articles about innovations in Python, about authors and editors of articles.
It saves data in the format _"Link to Article","Title","Editor, Author"_
- Documentation is taken from the link https://docs.python.org/3/whatsnew/
- The parser is implemented in the function ___whats_new()__  (main.py_)

----
### <anchor>Second parser. Python versions</anchor>
Parser for collecting information about Python versions - numbers, statuses (_in development, pre-release, stable, and etc_) and links to documentation.
The parser implementation uses _regular expressions (__regex___)
- Documentation location https://docs.python.org/3/
- The parser is implemented in the function ___latest_versions()__ (main.py_)
----
### <anchor>Third parser. Downloading files</anchor>
The parser downloads the documentation of the latest version of Python to the local machine _(archive with documents in PDF format (A4 paper size))_
- Documentation location https://docs.python.org/3/download.html
- The parser is implemented in the function ___download()__ (main.py_)
----
### <anchor>Fourth parser. Parsing PEP documents</anchor>
The parser collects information about PEP documents, compares the statuses of documents in a general table and in an individual card. If the information does not match, it makes an entry in the logs.
It also saves information about the number of documents with one or another status to the _csv_ file, counts their total number.
- PEP documentation location https://peps.python.org/
- The parser is implemented in the function ___pep()__ (main.py_)
----
### <anchor>Instruction to start</anchor>
<details>

1. Clone the repository to the local machine `git clone git@github.com:Andrey-Kugubaev/bs4_parser_pep.git`
2. Install and activate the virtual environment `python -m venv venv` or `python3 -m venv venv`
then `source venv/Scripts/activate` or `source venv/bin/activate`
3. Install Dependencies `pip install -r requirements.txt`
4. Run all parsers `python src/main.py` or some parser `python src/main.py pep`
(`python src/main.py whats-new`/`python src/main.py latest-versions`/
`python src/main.py download`)

</details>