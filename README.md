# EWB Phishing URL Awareness Checker

## Overview
This beginner-friendly Python command-line project checks the **text** of a URL for selected phishing warning signs. It is a defensive learning tool: it does not open links, contact websites, or send data anywhere.

## Features
- Detects an `@` symbol in the URL
- Flags unusually long URLs (over 100 characters)
- Flags IPv4-looking hostnames
- Flags hostnames with 5 or more dot-separated segments
- Flags punycode-style hostnames containing `goo--`
- Flags the HTTP scheme
- Repeats checks until the user enters `q`, `quit`, or `exit`
- Handles malformed URL input without crashing
- Prints a cautious review summary when warning signs are found

## Requirements
- Python 3.10 or later
- No extra packages

## Project structure
```text
phishing-url-awareness/
├── phishing_checker.py
├── README.md
├── requirements.txt
├── tests/
│   └── test_samples.md
└── screenshots/
    ├── sample_run.png       # Add your real terminal screenshot
    └── test_results.png     # Add your real test evidence screenshot
```

## How to run
Open a terminal in this project folder.

**Windows**
```bash
python phishing_checker.py
```

If `python` is not recognised, try `py phishing_checker.py`.

**Mac / Linux**
```bash
python3 phishing_checker.py
```

Enter one of the sample URLs from `tests/test_samples.md`. Run another check, or type `q` to quit.

## Example
Input:
```text
http://192.0.2.10/account
```

Expected output:
```text
Result:
- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.

REVIEW CAREFULLY: 2 warning sign(s) found.
Never enter passwords from unexpected links.
```

## Testing
Run the five sample inputs listed in [`tests/test_samples.md`](tests/test_samples.md) and record the actual output from your computer. Do not claim a test passed until you have run it.

## Improvements
1. **Repeat-check loop:** The program accepts multiple URLs in one session and exits with `q`, `quit`, or `exit`.
2. **Malformed-input handling:** URL parsing is wrapped in `try/except ValueError`, so malformed input such as `http://[bad` produces a clear message instead of stopping the program.
3. **Review summary:** When warning signs are detected, the program displays the number found and asks the user to review carefully.

## Limitations
This program checks only six visible text patterns. It does not visit URLs, scan for malware, query reputation services, or prove that a URL is safe. **No listed warning signs found does NOT mean a URL is safe.** HTTPS alone does not prove that a site is honest.

## Ethical use
- Use only the reserved sample strings in the workbook for testing.
- Do not collect credentials or send phishing messages.
- Do not scan or probe websites or networks without written authorisation.
- Never commit passwords, API keys, tokens, or private data.

## Screenshots
After running the program and completing your tests, save your own screenshots as:
- `screenshots/sample_run.png`
- `screenshots/test_results.png`

The screenshots must show real results from your computer. Do not use fabricated screenshots.

## Author
[Amresh Choudhary]  
[ Course : AI with cybersecurity]  
EWB Courses
