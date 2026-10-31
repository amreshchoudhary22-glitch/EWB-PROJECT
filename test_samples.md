# Test Results

Python version used: [fill in]  
Operating system: [fill in]  
Date: [fill in]

Run the program once per sample. Record the actual messages shown on your computer and mark PASS or FAIL honestly.

| # | Input | Expected result | Actual result | Pass/Fail |
|---|---|---|---|---|
| 1 | `https://www.example.com/login` | No listed warning signs; this is not a safety guarantee | [record actual output] | [PASS/FAIL] |
| 2 | `http://192.0.2.10/account` | IP-address hostname + HTTP | [record actual output] | [PASS/FAIL] |
| 3 | `http://example.com@sample.invalid/login` | `@` symbol + HTTP | [record actual output] | [PASS/FAIL] |
| 4 | `https://a.b.c.d.e.example.invalid/path` | Many hostname segments | [record actual output] | [PASS/FAIL] |
| 5 | `https://xn--example.invalid/` | Punycode-style hostname | [record actual output] | [PASS/FAIL] |

## Additional improvement checks

| Input / action | Expected behaviour | Actual result | Pass/Fail |
|---|---|---|---|
| `http://[bad` | Prints `This text is not a valid URL format.` and continues | [record actual output] | [PASS/FAIL] |
| Enter `q` | Prints goodbye and exits | [record actual output] | [PASS/FAIL] |

## Notes
[Write 2-3 lines about what you learned and what surprised you.]
