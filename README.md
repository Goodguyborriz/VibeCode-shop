# VibeCode-shop
CZ: Interaktivní didaktická aplikace pro výuku webových technologií, architektury klient-server a bezpečnosti na SŠ. Gamifikované mise přes DevTools (F12).  EN: Educational web app for high school computer science: learning client-server architecture, DOM manipulation, and web security through hands-on hacking.


# 🛒 VibeShop – Vibecoded Edition (Didaktická laboratoř)

> *"Proč stavět backend a platit za databázi, když máme front-end, DevTools a Google Forms?!"*  
> — Anonymní vibecoder před prvním velkým průšvihem

**VibeShop** je záměrně zranitelná, interaktivní jednostránková webová aplikace navržená pro **výuku informatiky na středních školách**. Vizuálně působí jako moderní a nablýskaný e-shop s elektronikou, pod kapotou však obsahuje ty nejabsurdnější architektonické chyby, které vznikají, když někdo postaví aplikaci bez pochopení architektury **klient–server** a zabezpečení svěří front-endu.

Studenti si v roli „etických hackerů“ vyzkouší práci se skutečnými vývojářskými nástroji prohlížeče (**DevTools / F12 / Inspect**) a na vlastní kůži pochopí, proč klientský kód nikdy nesmí nahrazovat backendovou logiku.

---

## 🎯 Proč tento projekt vznikl?

Klasická výuka bezpečnosti a webových technologií často končí u suché teorie o protokolech nebo omezování práv. VibeShop volí opačný přístup: **gamifikovanou destrukci**:
* **Okamžitá zpětná vazba:** Aplikace sleduje manipulaci s DOMem i lokálním úložištěm v reálném čase.
* **Žádná cheat tlačítka:** Žádná automatická klikátka – studenti musí otevřít skutečný inspektor, prozkoumat kód, upravit hodnoty nebo spustit příkaz v konzoli.
* **100% Client-Side Sandbox:** Celý projekt je obsažen v jediném souboru `index.html`. Nevyžaduje žádný server, Node.js ani databázi – běží offline nebo přímo z **GitHub Pages**.
* **Bezpečná fiktivní data:** Registrační brána i fiktivní tabulka hesel běží v izolovaném sandboxu bez odesílání citlivých údajů žáků.

---

## 🕵️ Seznam výukových misí (Challenges)

Aplikace obsahuje 6 cílů, které studenty provedou různými záložkami nástrojů pro vývojáře:

| # | Mise | Použitý nástroj v DevTools | Architektonický princip |
|---|---|---|---|
| **1** | **Cenový kouzelník** | *Elements / Inspector* | Manipulace se skrytými formulářovými prvky (`<input type="hidden">`). Cena se musí počítat na serveru! |
| **2** | **Matematický paradox** | *Elements / Inspector* | Obcházení klientských limitů formuláře (`min="1"`). Nákup záporného počtu kusů přičte kredit do peněženky. |
| **3** | **Tajný kód ve skriptu** | *Sources / Page Source* | Hardcoded slevové kupóny v klientském JavaScriptu (`shop-logic.js`). Tajná data nepatří do front-endu. |
| **4** | **Data Leak v API** | *Network / Fetch / JSON* | Overfetching a nefiltrovaná data – API vrací privátní záznamy i telemetrii, které se v UI nezobrazují. |
| **5** | **Okamžitý Administrátor** | *Console / Application* | Ukládání bezpečnostních rolí do `localStorage`. Změna `is_admin = true` v konzoli okamžitě odemkne Admin trezor. |
| **6** | **Databáze v Google Tabulkách** | *Sources / Elements* | Veřejně přístupná databáze hesel v plaintextu bez šifrování a solení. |

---

## 🚀 Jak aplikaci spustit

### Možnost A: GitHub Pages (Nejjednodušší pro třídu)
1. Forkněte si nebo nahrajte tento repozitář na svůj GitHub.
2. V nastavení repozitáře přejděte do **Settings -> Pages**.
3. Jako zdroj zvolte větev `main` (kořenový adresář `/root`) a uložte.
4. Odkaz na publikovanou stránku (např. přes zkracovač URL) promítněte studentům na tabuli.

### Možnost B: Lokální spuštění
1. Stáhněte soubor `index.html`.
2. Dvakrát na něj klikněte – otevře se v libovolném moderním prohlížeči (Chrome, Firefox, Edge, Safari). Nevyžaduje internetové připojení.

---

## 👩‍🏫 Pedagogická reflexe do hodiny

Po splnění misí doporučujeme otevřít se třídou diskusi na téma:

1. **Zlaté pravidlo vývoje webu:** *„Co pošle server do prohlížeče, to uživatel plně vlastní a ovládá.“*
2. **K čemu slouží front-end?** Klientská validace (červený rámeček při špatném e-mailu) slouží pouze pro uživatelský komfort, nikoliv pro bezpečnost.
3. **Jak by to mělo fungovat správně?**
   * Server přijímá z košíku pouze ID produktu a počet kusů; cenu si dohledá sám ve své autoritativní databázi.
   * Všechny matematické operace (součet, slevy, DPH) probíhají výhradně na backendu.
   * Uživatelská oprávnění a role se ověřují kryptograficky podepsanou session / JWT tokenem, nikoliv prostou proměnnou v prohlížeči.
   * Hesla se nikdy neukládají v plaintextu, ale hašují se pomocí bezpečných funkcí (bcrypt, Argon2) se solí.

---

## 📄 Licence

Tento projekt je šířen pod svobodnou licencí **MIT**. Můžete jej libovolně upravovat, rozšiřovat a využívat ve výuce na jakékoliv škole.
