# Test Results

Python version used: [fill after running] | Operating system / app: [fill] | Date: [fill]

| # | Input | Expected result | Actual result | Pass/Fail |
|---|---|---|---|---|
| 1 | `https://www.example.com/login` | No listed warning signs; reminder that this does not prove safety | No listed warning signs found. This does NOT prove safety. | PASS after verifying |
| 2 | `http://192.0.2.10/account` | IP address + HTTP warnings | Uses an IP address instead of a familiar domain.; Uses HTTP. HTTPS alone does not prove trust. | PASS after verifying |
| 3 | `http://example.com@sample.invalid/login` | @ symbol + HTTP warnings | Contains an @ symbol; inspect carefully.; Uses HTTP. HTTPS alone does not prove trust. | PASS after verifying |
| 4 | `https://a.b.c.d.e.example.invalid/path` | Many hostname segments warning | Contains many hostname segments/subdomains. | PASS after verifying |
| 5 | `https://xn--example.invalid/` | Punycode-style hostname warning | Contains a punycode-style hostname. | PASS after verifying |

## Notes

- I learned that URL text can contain clues such as `@`, an IP address, many hostname segments, punycode, or plain HTTP.
- The tool only checks six visible warning signs. It does not visit a website or prove that a URL is safe.

**Important:** Run all five samples yourself. Confirm the actual output and replace the provisional PASS labels if your results differ. Record your real Python version, device/app, and date before submitting.
