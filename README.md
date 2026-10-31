# EWB Phishing URL Awareness Checker

## Overview
Phishing is a trick that uses fake links or messages to make people share passwords, OTPs, or payment details. This beginner Python project reads URL text and points out selected warning signs. It does not open the URL or send information over the internet.

## Features
- Detects an `@` symbol in the URL
- Flags URLs longer than 100 characters
- Flags IPv4-address hostnames
- Flags hostnames with 5 or more dot-separated segments
- Flags punycode-style hostnames containing `xn--`
- Flags the HTTP scheme
- Repeats checks until the user types `q`, `quit`, or `exit`
- Handles malformed URL input without stopping unexpectedly
- Prints a “REVIEW CAREFULLY” summary when warning signs are found

## Requirements
- Python 3.10 or later
- No extra packages required

## How to Run
Open a terminal in this folder.

Windows:
```bash
python phishing_checker.py
```

Mac/Linux:
```bash
python3 phishing_checker.py
```

On a mobile device, use a Python environment that supports running a local `.py` file, or use a browser-based Python workspace. Do not use real suspicious links; use only the sample strings below.

## Example
```text
EWB Phishing URL Awareness Checker
Text checks only - this program does not open URLs.

Enter a sample URL (or type q to quit): http://192.0.2.10/account

Result:
- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.

REVIEW CAREFULLY: 2 warning sign(s) found.
Never enter passwords from unexpected links.
```

## Testing
See [`tests/test_samples.md`](tests/test_samples.md). Run all five sample inputs yourself and confirm the actual output before submission.

## Improvements
1. **Repeat checks with a quit command** — the user can check several sample URLs without restarting the program. Tested by entering multiple samples and then `q`.
2. **Malformed URL handling** — parsing errors return a clear message instead of crashing. Tested with the sample `http://[bad`.
3. **Review summary** — the program counts warning messages and prints a caution when warning signs are found.

## Screenshots
After running the program, save genuine screenshots of your own run:
- `screenshots/sample_run.png` — terminal/app showing the program, sample input, and output.
- `screenshots/test_results.png` — evidence of all five tests, or your completed test table.

Do not submit illustrative or edited images as proof of a real run.

## Limitations
This is an educational tool. It only reads URL text. It does not visit URLs, scan for malware, query reputation services, or prove that a URL is safe. “No listed warning signs found” does **not** mean a URL is safe. HTTPS alone does not prove a website is trustworthy.

## Ethical Use
Use the sample strings in the workbook. Do not collect credentials, send phishing messages, or probe websites without written permission. Never upload passwords, API keys, or confidential data to GitHub.

## Author
[Your name] — [Batch/course]
