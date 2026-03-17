# VIRTUAL ATIS
## A new way to communicate in the air.
--- 
## Project Structure

This repository is organized to separate data fetching from human-readable formatting.

<pre>
virtual-atis/
├── .gitignore               # Prevents committing junk/secrets
├── requirements.txt         # Project dependencies
├── README.md                # Project overview and setup
├── .env                     # Private API keys (CheckWX)
│
├── src/                     # Source code
│   ├── __init__.py          
│   ├── main.py              # Entry point (Coordinates the system)
│   ├── fetcher.py           # Data Architect: API calls to NOAA/CheckWX
│   ├── parser.py            # Data Architect: Raw METAR -> Python Dict
│   └── formatter.py         # Translator: Dict -> Human-readable text
│
├── tests/                   # Unit tests for logic
│   ├── __init__.py
│   ├── test_fetcher.py
│   └── test_parser.py
│
└── data/                    # Sample METAR strings for offline testing
    └── samples.json
</pre>

--- 

## Getting Started

To start, please install the required libraries for the project:
Bash

```pip install -r requirements.txt```

### Libraries included:

    Requests: For fetching real-time weather data.

    Python-metar: For decoding technical aviation abbreviations.

    Python-dotenv: For secure management of API keys.