# Revenue Analytics: E-commerce Growth Analysis

**Stack:** Python · DuckDB · SQL · pandas · scikit-learn · seaborn · Jupyter  
**Data:** 47,000+ transactions · 5,000+ customers · 18 months · 10 countries

---

## English Version

### Project Overview
47,000+ transactions · 5,000+ customers · April 2024 – October 2025 · 10 countries · 5 channels
B2B/B2C software reseller — Microsoft, Adobe, Salesforce, Notion, Tableau and others.
Products: annual subscriptions, monthly subscriptions, one-time licenses.
Channels: Website, Affiliate, Paid Search, Organic, Social, Retail Media, Email.
Markets: US, UK, Canada, Australia, Germany, France, Spain, Netherlands, Philippines, Brazil.

### Key Insights
*   **The Growth Bottleneck:** Revenue peaked in mid-2024 because user growth, order frequency, and average order value all leveled off at the same time. This is not a seasonal dip, but a structural limit.
*   **The ARPU Paradox:** All channels show a similar average order value ($647–$690). However, the Website channel drives 3x the revenue per user ($3,558) compared to Partners ($1,132). The growth isn't in the size of the first order, but in repeat purchase behavior.
*   **The Activation Problem:** Nearly half of our new customers (49%) don't come back after their first month. Improving our onboarding process to keep just 15% more of these customers would result in an extra $783,000 in annual revenue per cohort without additional ad spend.
*   **High-Cost Churn:** Our "Enterprise" segment acquired via Paid Search is failing, with a 47.6% churn rate. We are spending the most to acquire these customers, but they are the least loyal.

### Visual Analysis
![Monthly Net Revenue](images/monthly_revenue.png) ![Refund Rate by Category and Country](images/refund_heatmap.png)
![Retention](images/retention.png)

### Strategic Recommendations
1.  **Shift Budget:** Move 25% of the budget from Paid Search for Enterprise to the Website and Affiliate channels, which have proven long-term value.
2.  **Fix Refund Hotspots:** We lose money in specific country/product combinations (e.g., Services in the UK, Monitoring in Germany). Instead of changing prices, we must fix the product messaging to match customer expectations.
3.  **Proactive Renewal Management:** Since 88% of our revenue is annual subscriptions, we are at risk of a "renewal cliff." I recommend tracking the Renewal-to-New revenue ratio as our most important monthly metric.
4.  **Protect High-Value Customers:** Use our RFM segmentation to identify high-revenue customers ($15k+) and assign them dedicated support 60 days before their subscription ends.

### Revenue Forecasting & Trend Analysis
![Revenue Forecast](images/revenue_forecast.png)
*   **Methodology:** I implemented **Facebook Prophet** to model monthly revenue trends across key acquisition channels.
*   **The Insight:** The model identifies a clear divergence between the historical growth trend and the actual performance observed in late 2025. 
*   **Business Impact:** The "forecast" highlights that even with historical growth patterns, the current performance is underperforming the baseline. This is a quantitative proof that the business needs an immediate strategic pivot rather than waiting for "seasonal recovery."

---

## Tools & Methods
*   **DuckDB + SQL:** High-performance data aggregation for cohort and funnel analysis.
*   **Prophet (Meta):** Time series forecasting to model revenue trends, account for seasonality, and identify growth gaps.
*   **scikit-learn:** RFM clustering (KMeans) for customer segmentation and Random Forest for churn prediction (77.9% accuracy).
*   **pandas & seaborn:** Data cleaning, cohort matrix construction, and advanced visualization.
---

## Українська версія

### Огляд проекту
Цей проект — глибокий аналіз доходів реселера програмного забезпечення. Після швидкого росту на початку 2024 року бізнес вийшов на плато, яке тривало 14 місяців. Моєю метою було не просто зробити звіт, а знайти конкретні причини цієї стагнації та запропонувати план дій.

### Основні висновки
*   **Проблема росту:** Дохід перестав зростати, тому що зупинилися всі три головні драйвери: притік нових користувачів, частота покупок та середній чек. Це структурна проблема, а не сезонність.
*   **Парадокс ARPU:** Середній чек у всіх каналах майже однаковий ($647–$690). Проте канал Website приносить втричі більше доходу на одного клієнта ($3,558), ніж партнерські канали ($1,132). Ріст криється в тому, що клієнти вебсайту повертаються частіше.
*   **Проблема онбордингу:** 49% клієнтів не повертаються після першого місяця. Якщо ми покращимо процес активації та втримаємо хоча б на 15% більше клієнтів, це принесе додаткові $783,000 річного доходу без витрат на рекламу.
*   **Відтік Enterprise:** Ми витрачаємо найбільше на залучення Enterprise-клієнтів через платний пошук, але вони мають найвищий відтік — 47.6%. Ця стратегія зараз збиткова.

### Стратегічні рекомендації
1.  **Перерозподіл бюджету:** Варто забрати 25% бюджету з Paid Search і перенаправити на Website та Affiliate, які показують найкраще утримання.
2.  **Виправлення помилок:** Високий рівень рефандів у певних країнах (наприклад, UK або Німеччина) вказує на те, що клієнти очікують від продукту не того, що отримують. Потрібно змінити опис продукту, а не ціну.
3.  **Управління підписками:** Оскільки 88% нашого доходу — це річні підписки, ми ризикуємо зіткнутися з різким падінням доходу через 6-12 місяців, якщо не почнемо відстежувати поновлення зараз.
4.  **Фокус на цінних клієнтах:** Потрібно виділити топ-клієнтів (дохід $15k+ на клієнта) і працювати з ними персонально за 60 днів до закінчення терміну підписки.

---

### Tools & Methods
*   **DuckDB + SQL:** Використовував SQL всередині Python для швидкої обробки великих масивів даних.
*   **RFM-сегментація:** KMeans кластеризація для виділення найцінніших клієнтів.
*   **Прогнозування:** Random Forest модель для прогнозування відтоку клієнтів (точність 77.9%).
*   **Revenue Decomposition:** Моделювання доходу через формулу (Користувачі × Частота × Чек) для пошуку точок стагнації.

*Dataset: DataDNA Dataset Challenge — E-commerce Dataset, November 2025*
