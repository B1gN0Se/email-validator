RFC822 Email Validator
=====================

A simple, offline Python tool for validating email addresses against the RFC822 standard.
Perfect for quick checks, integration into scripts, or security testing of email input fields.

Features
--------
- RFC822-compliant: Uses a regular expression closely matching the RFC822 specification.
- Offline: No network connection required.
- Easy to use: Just run the script and enter an email address.
- Security Testing: Useful for testing input validation, including XSS payloads.

Usage
-----

```sh
git clone https://github.com/b1gn0se/email-validator.git
```

```sh
cd email-validator
```

```sh
python3 email-validator.py
```

Example
-------
$ python3 email-validator.py  
Enter email address: test@example.com  
RFC822 valid: YES

$ python3 email-validator.py  
Enter email address: "><script>alert(1)</script>@test.com  
RFC822 valid: NO  

Security Testing
----------------
You can use this tool to test how your application handles potentially malicious email input, such as XSS payloads.
Example payloads to try:
- "><script>alert(1)</script>@test.com
- "><svg/onload=alert(3)>@test.com
- "><svg/onload=confirm(1337)>"@x.y

Requirements
------------
- Python 3.x

---
Inspired by the classic RFC822 email validation tools and designed for modern security testing workflows.
