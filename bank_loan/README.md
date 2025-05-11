# 📊 Projekt: Dashboard bankovních půjček

## Kontext
Společnost poskytující osobní půjčky potřebuje přehledné a interaktivní řešení pro sledování a analýzu svých půjček.  
Vzhledem k velkému množství žádostí a financovaných částek je důležité mít nástroj umožňující sledování klíčových metrik a trendů v čase.

## Cíl projektu
Cílem projektu je vytvořit vizuálně přehledný a interaktivní dashboard pomocí **Power BI**, který umožní managementu:
- Sledovat celkový počet žádostí o půjčku
- Kontrolovat celkovou financovanou částku a přijaté platby
- Vyhodnocovat průměrnou úrokovou sazbu a DTI (Debt-to-Income)
- Analyzovat trendy podle data vydání půjčky
- Porovnávat data mezi měsíci (MTD, MoM)
- Rozlišovat mezi různými stavy půjček (splacené, po splatnosti, defaultní)

## Data
- 38 576 záznamů

---

## 📈 Požadavky na KPI
- **Total Loan Applications** (počet žádostí)
  - Počet žádostí od začátku měsíce (MTD)
  - Měsíční změny (MoM)
- **Total Funded Amount** (vyplacená částka)
  - Celková vyplacená částka od začátku měsíce (MTD)
  - Měsíční změny (MoM)
- **Total Amount Received** (přijatá částka)
  - Přijatá částka od začátku měsíce (MTD)
  - Měsíční změny (MoM)
- **Average Interest Rate** (průměrná úroková sazba)
  - Průměrná sazba od začátku měsíce (MTD)
  - Měsíční změny (MoM)
- **Average Debt-to-Income Ratio (DTI)**
  - Průměrný DTI od začátku měsíce (MTD)
  - Měsíční změny (MoM)

---

## 📊 Tabulka: Stav půjčky (Loan Status)
Tabulka obsahuje tyto metriky:
- Celkový počet žádostí
- Celková vyplacená částka
- Celková přijatá částka
- Vyplacená částka od začátku měsíce (MTD)
- Přijatá částka od začátku měsíce (MTD)
- Průměrná úroková sazba
- Průměrný DTI

---

## 📉 Vizualizace
- **Monthly Trends by Issue Date**: identifikace sezónnosti a dlouhodobých trendů v úvěrových aktivitách
- **Loan Term Analysis**: rozložení půjček podle délky splatnosti
- **Employee Length Analysis**: vztah mezi délkou zaměstnání a žádostmi o půjčku
- **Loan Purpose Breakdown**: rozdělení účelu půjček
- **Home Ownership Analysis**: vliv vlastnictví nemovitosti na schválení půjčky

---

## 🎯 Přínos
- Okamžitý přehled o výkonnosti portfolia půjček
- Odhalení sezónních trendů a regionálních rozdílů
- Efektivnější rozhodování založené na datech

---

## ⚙️ Použité funkce v Power BI
- `SUM`, `COUNT`, `IF`
- `AVERAGE`
- `TOTALYTD`, `TOTALMTD`
- `CALCULATE`
- `SAMEPERIODLASTYEAR`
- `CONCATENATE`
- `DATESMTD`
- `DATEADD`

---
