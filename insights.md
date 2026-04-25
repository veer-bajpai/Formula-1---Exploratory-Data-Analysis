# 💡 Key Insights — Formula 1 EDA

A summary of the most interesting findings from the exploratory data analysis of Formula 1 historical data (2009–2017).

---

## 🌍 Circuits

- **USA leads in circuit count** — The United States hosts the highest number of F1 circuits, reflecting its long and varied motorsport history across different eras of the sport.
- **British Grand Prix is the most hosted** — The British Grand Prix at Silverstone has been held more times than any other race on the calendar, cementing the UK's central role in F1 history.
- **Marine West Coast climate dominates** — The majority of F1 circuits sit in Marine West Coast climate zones, particularly across Western Europe (UK, Belgium, Germany, France). This directly influences race conditions — typically cool, overcast, and occasionally wet.
- **Global spread is uneven** — The majority of circuits are concentrated in Europe, with Asia, the Americas, and the Middle East being significantly underrepresented. Africa has virtually no F1 presence.

---

## 🧑‍🏎️ Drivers

- **Lewis Hamilton dominates the modern era** — Among drivers active after 2010 with 100+ race starts, Hamilton stands out with the highest average points per race and one of the largest total point accumulations.
- **Sebastian Vettel is a close rival** — During the 2010–2013 period, Vettel's Red Bull dominance is clearly visible in the bubble chart, with a very high total points haul across that stretch.
- **Veteran drivers come predominantly from the UK and Brazil** — Drivers born before 1985 are heavily represented by British and Brazilian nationalities, reflecting the traditional powerhouses of the sport.
- **Younger generation is more globally diverse** — Drivers born after 1985 show a much wider spread of nationalities, including strong representation from Germany, France, Finland, and Australia — pointing to F1's growing international footprint.
- **Pit stop speed is tightly contested at the top** — The fastest pit stop times cluster within a very narrow range (under 3 seconds in many cases), showing that modern F1 pit crews operate at an extraordinarily consistent elite level.

---

## 🏗️ Constructors

- **British constructors dominate by nationality** — The UK produces more F1 constructors than any other country by a wide margin, driven by the "Motorsport Valley" cluster in the English Midlands where most top teams are based.
- **Ferrari leads all-time race wins** — Ferrari appears at the top of both the race win bar chart and the points accumulation chart, underlining its unrivalled longevity and competitiveness in the sport.
- **McLaren, Williams, and Red Bull are close rivals** — These three teams trail Ferrari in wins but maintain a significant gap over the rest of the field, forming a clear "big four" in terms of historical dominance.
- **Points accumulation is highly concentrated** — When plotting total points by constructor over all seasons, a long tail is visible: the top 5–6 teams account for the overwhelming majority of all points ever scored, while the rest of the grid are separated by a massive gap.
- **Red Bull's rise is sharp and recent** — Red Bull's total points climb steeply in the post-2010 period, driven almost entirely by their four consecutive championship-winning seasons (2010–2013).

---

## 📊 General Observations

- **The data covers 997 races** across 69 seasons, making it a broad but not complete historical record (2009–2017 window for most analyses).
- **426,000+ lap time records** make the lap timing dataset the richest in the collection — a goldmine for deeper time-series analysis or predictive modelling.
- **Missing data is minimal** — The altitude field in `circuits.csv` was the primary missing-data issue (72/73 values absent), and was dropped cleanly with no downstream impact.
- **Pit stop data only begins from 2011** — The `pitStops.csv` dataset is partial, which limits historical comparisons of pit strategy evolution.
