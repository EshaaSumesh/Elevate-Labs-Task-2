# 📧 Phishing Email Analysis Project

## 🛡️ Objective
This project focuses on analyzing a suspicious phishing email sample to identify and document the phishing techniques used. The goal is to develop awareness and detection skills using freely available tools.

---

## 🧰 Tools Used

- 📄 `.eml` file viewer: [Zoho EML Viewer](https://www.zoho.com/toolkit/eml-viewer.html)
- 🧪 [MxToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)
- 🔍 Manual inspection of the email body (HTML source analysis)

---

## 📁 Email Sample Analyzed

- **File:** `phish.eml`
- **Impersonated Brand:** Microsoft
- **Main Claim:** "Unusual sign-in activity detected on your Microsoft account"
- **Sender Email:** `sotrecognizd@gmail.com` (used in all embedded mailto: links)

---

## 🔍 Phishing Indicators Identified

| No | Indicator | Description |
|----|-----------|-------------|
| 1️⃣ | **Spoofed Branding** | Claims to be Microsoft, but uses a Gmail address: `sotrecognizd@gmail.com`. |
| 2️⃣ | **Authentication Failures** | DMARC, SPF, and DKIM all failed (based on MxToolbox header analysis). |
| 3️⃣ | **Suspicious `mailto:` links** | Links like `mailto:sotrecognizd@gmail.com` disguised as “Report the User” or “Unsubscribe”. Used to verify active users. |
| 4️⃣ | **Scare Tactic** | Claims someone from Russia logged in from Windows 10 & Firefox — used to provoke panic. |
| 5️⃣ | **Tracking Pixel** | A hidden 1×1 pixel image embedded: `http://thebandalisty.com/track/...` — often used to detect when a user opens the email. |
| 6️⃣ | **Generic Language** | No use of the user’s real name. Just “your Microsoft account” and "Dear Customer". |
| 7️⃣ | **Minor Grammar Issues** | “Unusual sign.in activity” uses an incorrect period; language is robotic and slightly off-brand. |


---

## ✅ Key Learnings

- `.eml` files contain rich metadata and embedded links that are crucial for phishing analysis.
- Mailto links can be used for more than replies — they can confirm valid email addresses to attackers.
- Header authentication results (SPF/DKIM/DMARC) are useful for verifying sender legitimacy.
- Branding spoofing is common and convincing — users must examine sender addresses and domain carefully.
- Tools like Zoho's EML viewer make it easy to dissect phishing emails safely.



## ⚠️ Disclaimer

This analysis is for educational purposes only.  
Do not interact with suspicious emails or links unless you are in a secure, sandboxed or offline environment.





