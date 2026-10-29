# Test-Result

**Python version used:** Python 3.14.7  
**Operating system:** Linux  
**Date:** 2026-10-29

## Test Results

| Input | Expected result | Actual result | Pass/Fail |
|---|---|---|---|
| 1: `https://www.example.com/login` | No listed warning signs | No listed warning signs found. This does NOT prove safety. | PASS |
| 2: `http://192.0.2.10/account` | IP address + HTTP | Uses an IP address instead of a familiar domain; Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 3: `http://example.com@sample.invalid/login` | @ symbol + HTTP | Contains an @ symbol; inspect carefully; Uses HTTP. HTTPS alone does not prove trust. | PASS |
| 4: `https://a.b.c.d.e.example.invalid/path` | Many hostname segments | Contains many hostname segments/subdomains. | PASS |
| 5: `https://xn--example.invalid/` | Punycode-style hostname | Contains a punycode-style hostname. | PASS |

## Notes
I have learnt how to detect common red flags within URLs using Python. A URL that does not have any red flags does not mean it is safe. Through this project I have gained an understanding of the basics behind phishing awareness and URL checking.
