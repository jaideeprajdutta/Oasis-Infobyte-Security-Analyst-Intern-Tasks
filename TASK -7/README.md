# Task 7 – Vulnerability Scanning with Nikto

## Target
- **Host:** 127.0.0.1 (DVWA)
- **Web Server:** Apache/2.4.65 (Debian)
- **Scan Tool:** Nikto v2.5.0

## Findings
1. **Missing Security Headers**
   - X-Frame-Options and X-Content-Type-Options headers not set.
   - Risk: Clickjacking and MIME-sniffing attacks.

2. **Directory Indexing Enabled**
   - /dvwa/config/, /dvwa/tests/, /dvwa/database/, /dvwa/docs/
   - Risk: Sensitive files exposed.

3. **Exposed .git Files**
   - .git/index, .git/config, .gitignore
   - Risk: Potential disclosure of source code and credentials.

4. **PHP Backdoors**
   - Found multiple suspicious PHP files (`server.php`, `Meuhy.php`, etc.)
   - Risk: Remote file access, code execution.

5. **Potential Remote Command Execution**
   - Exploitable paths allowing `cat /etc/hosts`.
   - Risk: Full system compromise.

## Recommendations
- Add missing security headers in Apache config.
- Disable directory indexing (`Options -Indexes`).
- Remove `.git` and sensitive files from web root.
- Audit and remove malicious PHP backdoors.
- Harden input validation and use prepared statements.
- Restrict access to phpMyAdmin and database directories.

## Conclusion
Nikto successfully identified **26 issues** in the DVWA target, including weak security headers, misconfigurations, exposed files, and backdoors. Remediation steps are necessary to secure the application against real-world attackers.
