# Test-Result

Python version used: Python 3.14.7 Operating system: Linux Date: 2026-10-29

#

Input                          |     Expected result     | Actual result                |  Pass/Fail

1:https://www.example.com/login| No listed warning signs |No listed warning signs found.
                                                          This does NOT prove safety.      |PASS

2:http://192.0.2.10/account    | IP address + HTTP   |Uses an IP address instead of a familiar domain; 
                                                     |Uses HTTP. HTTPS alone does not prove trust. |PASS

3:http://example.com@sample.
invalid/login                  | @ symbol + HTTP     |Contains an @ symbol; inspect carefully; 
                                                     |Uses HTTP. HTTPS alone does not prove trust. |PASS

4:https://a.b.c.d.e.example.
invalid/path                   |Many hostname segments|Contains many hostname segments/subdomains. |PASS

5:https://xn--example.invalid/ |Punycode-style hostname| Contains a punycode-style hostname.|PASS 



Notes

I learned how I can check the warning signs by using Python through URL text analysis.

I learned how @ symbol, IP addresses, HTTP, lengthy URLS, and abnormal host names can be considered helpful warning signs.

I learned that the absence of warning signs does not mean that a particular URL is completely safe.
