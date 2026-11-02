# Test Results

Python version used: [3.14.7]  
Operating system: [Windows 11 , Version 23H2]  
Date: [31-10-2026]

Run the program once per sample. Record the actual messages shown on your computer and mark PASS or FAIL honestly.

| # | Input | Expected result | Actual result | Pass/Fail |
|---|---|---|---|---|
| 1 | `https://github.com/login` | No listed warning signs; this is not a safety guarantee | [No listed warning signs found. This does NOT prove safety] | [PASS] |
| 2 | `https://accounts.google.com/signin` | IP-address hostname + HTTP |[No listed warning signs found. This does NOT prove safety] | [PASS] |
| 3 | `https://www.linkedin.com/login` | `@` symbol + HTTP | [No listed warning signs found. This does NOT prove safety] | [PASS] |
| 4 | `https://login.microsoftonline.com/` | Many hostname segments | [No listed warning signs found. This does NOT prove safety] | [PASS] |
| 5 | `https://www.facebook.com/login` | Punycode-style hostname | [No listed warning signs found. This does NOT prove safety] | [PASS] |

## Additional improvement checks

| Input / action | Expected behaviour | Actual result | Pass/Fail |
|---|---|---|---|
| `http://[bad` | Prints `This text is not a valid URL format.` and continues | [record actual output] | [PASS/FAIL] |
| Enter `q` | Prints goodbye and exits | [record actual output] | [PASS/FAIL] |

## Notes
I learned that phishing URLs often give themselves away through structure alone, such as an @ symbol, a raw IP address, or too many subdomains. What surprised me was that a URL with no warning signs still isn't proof of safety, so the tool can only point out red flags. I also found that malformed input like http://[bad crashes URL parsing unless it is handled with try/except.
