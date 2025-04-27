# portfolio_

# 📊 Dashboard bankovních půjček

## Projektový popis
Společnost poskytující osobní půjčky potřebuje přehledné a interaktivní řešení pro sledování a analýzu svých půjček. Cílem projektu je vytvořit dashboard v **Power BI**, který umožní:

- Sledovat celkový počet žádostí o půjčku
- Kontrolovat celkovou financovanou částku a přijaté platby
- Vyhodnocovat průměrnou úrokovou sazbu a poměr dluhu k příjmu (DTI)
- Analyzovat trendy podle data vydání půjčky
- Porovnávat data mezi měsíci (Month-to-Date, Month-over-Month)
- Rozlišovat mezi různými stavy půjček (splacené, po splatnosti, defaultní)

---

## 📈 KPI požadavky

- **Total Loan Applications**: Počet žádostí (MTD, MoM)
- **Total Funded Amount**: Vyplacená částka (MTD, MoM)
- **Total Amount Received**: Přijatá částka (MTD, MoM)
- **Average Interest Rate**: Průměrná úroková sazba (MTD, MoM)
- **Average Debt-to-Income Ratio (DTI)**: Průměrný DTI (MTD, MoM)

---

## 🛠️ Tabulky a metriky

| Stav půjčky | Celkový počet žádostí | Celková vyplacená částka | Celková přijatá částka | MTD financování | MTD příjem | Průměrná úroková sazba | Průměrný DTI |
|:------------|:----------------------|:-------------------------|:----------------------|:---------------|:----------|:------------------------|:------------|

---

## 📊 Vizualizace

- **Monthly Trends by Issue Date**: Identifikace sezónnosti a dlouhodobých trendů
- **Loan Term Analysis**: Analýza podle délky půjčky
- **Employee Length Analysis**: Vliv délky zaměstnání na schválení půjčky
- **Loan Purpose Breakdown**: Rozdělení účelů půjček
- **Home Ownership Analysis**: Vliv vlastnictví nemovitosti

---

## 🎯 Přínos
- Okamžitý přehled o výkonu portfolia půjček
- Odhalení sezónních trendů a regionálních rozdílů
- Podpora rozhodování založeného na datech

---

## ⚙️ Použité funkce v Power BI

- `SUM`, `COUNT`, `IF`, `AVERAGE`
- `TOTALYTD`, `TOTALMTD`
- `CALCULATE`, `SAMEPERIODLASTYEAR`
- `CONCATENATE`, `DATESMTD`, `DATEADD`

---

## 🗄️ Analýza pomocí SQL

### KPI’s:
```sql
SELECT COUNT(id) AS Total_Applications FROM bank_loan_data;
SELECT SUM(loan_amount) AS Total_Funded_Amount FROM bank_loan_data;
SELECT SUM(total_payment) AS Total_Amount_Collected FROM bank_loan_data;
SELECT AVG(int_rate) * 100 AS Avg_Int_Rate FROM bank_loan_data;
SELECT AVG(dti) * 100 AS Avg_DTI FROM bank_loan_data;
```

---

## 📈 Good Loan vs Bad Loan analýza

**Good Loan:** `Fully Paid` nebo `Current`  
**Bad Loan:** `Charged Off`

Výpočty procent a součtů dobrých a špatných půjček pomocí SQL dotazů.

---

## 🛠️ Další SQL analýzy

- Loan Status
- Monthly Trends
- Regionální analýza (STATE)
- Loan Term Analysis
- Employee Length Analysis
- Loan Purpose Analysis
- Home Ownership Analysis

---

## 🧩 Postup v Power BI

1. Vytvoření **Date Table** pomocí funkce `CALENDAR()`
2. Přidání sloupce **Month**
3. Nastavení vztahů mezi tabulkami
4. Vytvoření výpočtů a Measures
5. Rozdělení na Good Loan a Bad Loan skupiny
6. Vizuály: karty, koláče, spojnicové grafy, sloupcové grafy, stromové grafy

---

# 📌 Shrnutí
Tento dashboard poskytuje komplexní přehled o výkonu bankovních půjček, pomáhá při strategickém rozhodování a identifikuje klíčové oblasti růstu.
