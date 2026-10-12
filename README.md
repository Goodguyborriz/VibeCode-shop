# 🛒 VibeShop – Vibecoded Edition (Student Hacker Lab)

[🇨🇿 Česky](#-česká-verze) | [🇬🇧 English](#-english-version)

---

## 🇨🇿 Česká verze

> *"Proč stavět backend a platit za databázi, když máme front-end, DevTools a Google Forms?!"*  
> — Anonymní vibecoder před prvním velkým bezpečnostním incidentem

**Živá verze projektu (GitHub Pages):**  
👉 **[https://goodguyborriz-coder.github.io/VibeCode-shop/](https://goodguyborriz-coder.github.io/VibeCode-shop/)**

---

### 👤 Autor a kontext vzniku
* **Autor:** Mgr. Martin Žirovnický
* **Instituce:** Obchodní akademie Dušní, Praha 1 (OA Dušní)
* **Předmět:** Informační technologie
* **Určeno pro:** Žáky středních škol a vzdělávací iniciativy (např. *EU Code Week*)
* **Licence:** MIT License (volné šíření a úpravy pro vzdělávací účely)[cite: 2]

---

### 🎯 K čemu aplikace slouží?
**VibeShop** je interaktivní výuková webová laboratoř navržená speciálně pro **studenty středních škol**.

Cílem projektu je, aby si studenti prakticky a na vlastní kůži uvědomili **zásadní rozdíl mezi frontendem a backendem**:
* Vše, co vidí na obrazovce (HTML struktura, kaskádové styly i JavaScript běžící v prohlížeči), se odehrává a interpretuje **přímo na jejich vlastním zařízení**[cite: 1].
* Cokoliv běží na straně klienta, má uživatel plně pod kontrolou a může to libovolně modifikovat[cite: 1, 2].
* Klientská validace slouží výhradně pro uživatelský komfort, nikoliv pro bezpečnost. Veškeré finance, pravidla a práva musí autoritativně ověřovat backend na serveru[cite: 1, 2].

Aplikace na první pohled vypadá jako nablýskaný e-shop, ale pod kapotou záměrně obsahuje absurdní bezpečnostní chyby[cite: 2]. Studenti v roli „etických hackerů“ používají standardní vývojářské nástroje prohlížeče (**DevTools / F12 / Inspect**) a plní gamifikované úkoly[cite: 1, 2].

---

### 🎓 Vzdělávací cíle a naplnění RVP pro střední školy

Aktivita přímo rozvíjí očekávané výstupy revidovaného RVP (oblast **Informatika / Informační a komunikační technologie** na SŠ) a klíčové kompetence:

#### 1. Vazba na vzdělávací obsah RVP (Informatika)
* **Informační systémy a webové technologie:** Žák rozumí základnímu principu architektury klient–server, chápe roli webového prohlížeče jako klientského interpretu kódu a rozlišuje mezi lokálním zobrazením dat a jejich perzistentním uložením na serveru.
* **Digitální bezpečnost a etika:** Žák identifikuje zranitelnosti vznikající nedostatečným ověřováním vstupů na straně serveru, chápe rizika ukládání nešifrovaných dat (plaintext hesel) a v praxi si ověří zásady bezpečného zacházení s citlivými údaji v síťovém prostředí[cite: 1, 2].
* **Algoritmizace a porozumění kódu:** Žák se orientuje ve struktuře DOM stromu (HTML/CSS), čte a upravuje hodnoty proměnných v klientském skriptu (JavaScript) a testuje chování programu při nestandardních vstupech (např. záporné hodnoty)[cite: 1, 2].

#### 2. Rozvoj klíčových kompetencí
* **Digitální kompetence:** Žák efektivně ovládá diagnostické nástroje (vývojářskou konzoli, síťový analyzátor a DOM inspektor), chápe fungování digitálních technologií „pod povrchem“ grafického rozhraní a kriticky hodnotí bezpečnost webových služeb[cite: 1, 2].
* **Kompetence k řešení problémů:** Žák analyzuje chybně navržený systém, formuluje hypotézy o jeho fungování, praktickými pokusy ověřuje jeho limity a hledá způsoby, jak nežádoucímu chování předejít (návrh správného backendového řešení)[cite: 1, 2].
* **Kompetence k učení:** Žák propojuje teoretické koncepty síťové komunikace s reálnou interaktivní zkušeností a upevňuje si porozumění principu klientských a serverových rolí[cite: 2].

---

### 🕹️ Jak se to používá?

1. **Otevření v prohlížeči:**  
   Stačí otevřít odkaz na **[GitHub Pages](https://goodguyborriz-coder.github.io/VibeCode-shop/)** v libovolném moderním prohlížeči (Chrome, Firefox, Edge, Safari)[cite: 2]. Není potřeba nic instalovat ani konfigurovat backend[cite: 2].
2. **Překonání registrační brány:**  
   Při vstupu na studenty čeká absurdně dlouhý byrokratický dotazník plný povinných polí. Cílem je formulář nevyplňovat, ale v DevTools ho obejít (např. smazáním elementu `<div id="authGateWall">` v záložce *Elements* nebo použitím uniklých přihlašovacích údajů z konzole)[cite: 1].
3. **Plnění výukových misí:**  
   Kliknutím na tlačítko **Hacker Mise** v navigaci se otevře panel s podrobnými návody na 6 praktických úkolů[cite: 1]:
   * **Mise 1 – Cenový kouzelník (Elements):** Přepis skryté ceny (`<input type="hidden">`) v DOM stromu na 1 Kč[cite: 1, 2].
   * **Mise 2 – Matematický paradox (Elements / UI):** Zadání záporného počtu kusů do košíku – e-shop nákup proplatí[cite: 1, 2].
   * **Mise 3 – Tajný promo kód (Console):** Odhalení 100% slevy v otevřené JavaScript proměnné `PROMO_CODES_DATABASE`[cite: 1, 2].
   * **Mise 4 – Data Leak / Overfetching (Network):** Prozkoumání surové síťové odpovědi obsahující čísla platebních karet a hesla[cite: 1, 2].
   * **Mise 5 – Okamžitý Administrátor (Application / Console):** Přepsání hodnoty `localStorage.setItem('is_admin', 'true')` pro odemčení tajného admin trezoru[cite: 1, 2].
   * **Mise 6 – Databáze v paměti (Console):** Výpis všech hesel v čistém textu pomocí `console.table(userAccountsDb)`[cite: 1, 2].

---

### 👩‍🏫 Doporučená reflexe do hodiny
* **Zlaté pravidlo:** Co pošle server do prohlížeče, to uživatel vlastní[cite: 2].
* **Proč selhal klientský e-shop?** Protože se spoléhal na to, že uživatel kód v prohlížeči nezmění[cite: 1, 2].
* **Jak to dělá správný backend:** Klient posílá pouze ID zboží a počet kusů; cenu, slevy a celkový součet počítá výhradně server s autoritativní databází[cite: 1, 2].

---
---

## 🇬🇧 English Version

> *"Why build a backend and pay for a database when we have the front-end, DevTools, and Google Forms?!"*  
> — Anonymous vibecoder moments before their first massive security breach

**Live Demo (GitHub Pages):**  
👉 **[https://goodguyborriz-coder.github.io/VibeCode-shop/](https://goodguyborriz-coder.github.io/VibeCode-shop/)**

---

### 👤 Author & Context
* **Author:** Mgr. Martin Žirovnický
* **Institution:** Secondary School of Economics Dušní (OA Dušní), Prague, Czech Republic
* **Subject:** Information Technology
* **Audience:** High school students & coding initiatives (e.g., *EU Code Week*)
* **License:** MIT License[cite: 2]

---

### 🎯 What is this project for?
**VibeShop** is an interactive, intentionally vulnerable single-page web laboratory tailored for **secondary school students**[cite: 2].

Its primary pedagogical goal is to help students truly grasp the difference between **front-end and back-end architecture**:
* Everything rendered on screen (HTML, CSS, and client-side JavaScript) is running **locally on their machine**[cite: 1].
* Code executed in the browser is completely under the user's control and can be modified at will[cite: 1, 2].
* Client-side validation exists purely for user experience (UX), never for security. All financial calculations, permissions, and business rules must be authoritatively enforced by the back-end server[cite: 1, 2].

The web application masquerades as a sleek modern electronics store, but underneath it is packed with deliberate client-side vulnerabilities[cite: 2]. Students act as ethical hackers using standard browser developer tools (**DevTools / F12 / Inspect**) to complete hands-on missions[cite: 1, 2].

---

### 🎓 Educational Goals & Competencies (Framework Education Programme)
The activity aligns with modern secondary informatics curricula by fostering key digital competencies and algorithmic problem solving:
* **Client-Server Architecture:** Understanding the role of the web browser as a client-side code interpreter and distinguishing between client state and server persistence.
* **Cybersecurity & Data Privacy:** Discovering why client-side data validation is insecure, recognizing the risk of plaintext credentials, and experiencing data leaks firsthand[cite: 1, 2].
* **Digital Problem Solving:** Utilizing developer tools (DOM Inspector, Console, Network Tab) to dissect and manipulate web applications in a safe sandbox[cite: 1, 2].

---

### 🕹️ How to use it?

1. **Launch in Browser:**  
   Open the **[GitHub Pages link](https://goodguyborriz-coder.github.io/VibeCode-shop/)** in any modern desktop web browser (Chrome, Firefox, Edge, Safari)[cite: 2]. No installation, server, or database required[cite: 2].
2. **Bypass the Registration Gate:**  
   Upon opening the page, students are greeted by an absurdly tedious questionnaire full of mandatory fields. The challenge is not to fill it out, but to bypass it via DevTools (e.g., deleting `<div id="authGateWall">` in the *Elements* tab or logging in with leaked credentials found via the console)[cite: 1].
3. **Solve the Hacker Missions:**  
   Clicking the **Hacker Missions** drawer in the navigation bar reveals step-by-step guides for 6 interactive exploits[cite: 1]:
   * **Mission 1 – Price Wizard (Elements):** Tamper with the hidden input (`<input type="hidden">`) in the DOM to buy a high-end laptop for 1 CZK[cite: 1, 2].
   * **Mission 2 – Negative Quantity (Elements / UI):** Exploit missing server-side logic by ordering a negative item quantity, causing the shop to pay you[cite: 1, 2].
   * **Mission 3 – Secret Promo Code (Console):** Inspect the exposed client variable `PROMO_CODES_DATABASE` in the console to find a secret 100% discount code[cite: 1, 2].
   * **Mission 4 – Network Data Leak (Network):** Inspect an overfetched API response (`/api/v2/customer-reviews`) exposing sensitive credit card and plaintext password data[cite: 1, 2].
   * **Mission 5 – Privilege Escalation (Application / Console):** Set `localStorage.setItem('is_admin', 'true')` to unlock the classified root administrator vault[cite: 1, 2].
   * **Mission 6 – In-Memory Database (Console):** Dump all stored plain-text user passwords using `console.table(userAccountsDb)`[cite: 1, 2].

---

### 📄 License
This educational project is distributed under the **MIT License**. Feel free to fork, adapt, and use it in your classrooms[cite: 2].
