# Cross-Site Scripting (XSS) Security Assessment

##  Overview
Conducted a controlled Cross-Site Scripting (XSS) security assessment to identify and validate input validation vulnerabilities in a web application. The goal was to test how user-supplied data is handled, identify potential injection points, and provide remediation aligned with OWASP and secure coding standards.

This assessment was performed in a safe, authorized testing environment with explicit permission. No live production systems were targeted.

##  Objective
1.  Identify reflected and/or stored XSS vulnerabilities
2.  Assess the impact of executing unauthorized client-side scripts
3.  Provide risk-rated findings and practical mitigation recommendations
4.  Demonstrate understanding of secure development practices for banking/financial applications

##  Methodology
The assessment followed OWASP Testing Guide v4.2 methodology:
- **Recon & Input Mapping**: Identified all user input fields, URL parameters, and forms
- **Payload Testing**: Tested with common XSS vectors to check for improper output encoding
- **Impact Analysis**: Determined if scripts could access cookies, session tokens, or DOM
- **Reporting**: Documented findings with PoC, risk rating, and remediation steps

**Tools Used**: Burp Suite, Browser DevTools, OWASP ZAP

##  Key Findings Summary
| Vulnerability | Severity | Location | Impact |
| --- | --- | --- | --- |
| Reflected XSS in Search Parameter | High | `/search?q=` | Attacker can steal session cookies and hijack user accounts |
| Lack of Input Validation | Medium | Contact Form | Potential for script injection |

*Full technical details, screenshots, and PoC are in the attached report.*

##  Recommendations
Aligned to OWASP and Banks Secure Coding Standards:
1.  **Input Validation**: Validate and sanitize all user inputs server-side
2.  **Output Encoding**: Encode data before rendering in HTML, JS, URL contexts
3.  **Content Security Policy**: Implement CSP headers to block inline scripts
4.  **Secure Cookies**: Set `HttpOnly` and `Secure` flags on session cookies
5.  **Security Testing**: Integrate SAST/DAST into CI/CD pipeline

##  Banking Relevance
XSS is a top 10 OWASP risk and critical for financial institutions. 
An XSS flaw could lead to account takeover, data theft, and POPIA breaches. 
This project demonstrates the ability to identify, report, and recommend fixes for vulnerabilities that directly impact customer data protection and regulatory compliance.

##  Full Report
[Download Full XSS Assessment Report](https://drive.google.com/file/d/1TJzXHwRVaoFwVnJclIkzZ3_r5aQlLoj2/view?usp=drive_link)
https://drive.google.com/file/d/1TJzXHwRVaoFwVnJclIkzZ3_r5aQlLoj2/view?usp=drive_link

## Disclaimer
This assessment was conducted for educational and portfolio purposes only. All testing was done on authorized test environments. Do not attempt on systems without permission.

##  Skills Demonstrated
`Web Application Security` `OWASP Top 10` `Vulnerability Assessment` `Risk Reporting` `Secure Coding` `Burp Suite` `Threat Modeling`
