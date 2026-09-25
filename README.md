# FUTURE_CS_01
# Vulnerability Assessment Report — demo.testfire.net

Cyber Security Internship — Task 1 (2026)
Future Interns Cybersecurity Program

---
## ⚠️ Disclaimer

This project was carried out **strictly for educational and internship purposes** on
[`demo.testfire.net`](http://demo.testfire.net) — a **publicly available, intentionally
vulnerable demo banking site** ("Altoro Mutual") that is provided by HCL Technologies /
IBM specifically to demonstrate web application security scanning tools.

- **No real, private, or third-party website was targeted.**
- **No login bypass, exploitation, brute-force, or Denial-of-Service activity was performed.**
- All testing was **passive and read-only** — limited to port/service enumeration and
  inspection of publicly served response headers, exactly as permitted by the demo site's
  own terms of use.
- No protocol, law, or responsible-disclosure guideline was violated. This repository
  documents an **assessment methodology exercise**, not an attack on live infrastructure.

---

## 📌 About the Task

Every business today owns a website — but most websites are not secure. Small businesses,
startups, and agencies often use outdated software, misconfigure security headers, or
expose sensitive information unknowingly. Clients usually don't ask for hacking; they ask
for clarity: *"Is my website safe? What are the risks? What should we fix first?"*

This task is about learning to answer that question professionally — i.e. **security
consulting, not hacking.**

### Objective

- Analyze a public website for common security weaknesses
- Classify risks in a business-friendly way (Low / Medium / High)
- Explain issues clearly, without technical jargon overload
- Suggest practical, prioritized remediation steps
- Present everything in a professional audit report

### Scope & Ethics

| Allowed | Not Allowed |
|---|---|
| Public-facing pages only | Login bypass |
| Passive scanning | Exploitation |
| Header/configuration checks | Brute-force attacks |
| Read-only service enumeration | Denial-of-Service (DoS) |

The guiding principle throughout: **think like a security auditor, not an attacker.**

---

## 🛠️ Tools Used

| Tool | Purpose |

 **Nmap** (CLI + Zenmap GUI) | Port and service/version enumeration |
 **OWASP ZAP** (Passive Scan) | Identifying vulnerabilities without active exploitation |
 **Browser DevTools** (Firefox) | Inspecting HTTP response headers and cookies |
**Canva** | Designing the final report layout |

---

## 📂 Repository Contents

 File | Description |

| `Vulnerability_Assessment_Report_demo.testfire.net.pdf` | Full audit report — executive summary, scope & methodology, detailed findings, risk classification, remediation timeline, and conclusion |
| `Evidence_Appendix_demo.testfire.net.pdf` | Screenshot evidence (4 exhibits) with explanations, mapped to each finding in the report |
| `README.md` | This file |

---

## 🔍 Summary of Findings

| Vulnerability | Severity | Recommendation |

| Unencrypted HTTP Protocol | **High** | Deploy SSL/TLS and enforce HTTP → HTTPS redirect |
| Missing Security Headers (CSP, X-Frame-Options, HSTS) | **Medium** | Configure `X-Frame-Options: SAMEORIGIN` and `Strict-Transport-Security` |
| Server Version Disclosure (Apache-Coyote/1.1) | **Low** | Suppress server banner headers; verify Tomcat patch level |
| Unnecessary Open Port (8080) | **Low** | Restrict via firewall to authorized management IPs |

**Overall Risk Classification: Medium**

Full details, business-friendly explanations, and a phased remediation timeline
(0–7 / 7–14 / 14–30 days) are in the main report PDF.

---

## 👤 Author

Cybersecurity Intern — Future Interns Program
Assessment conducted: September 2026
