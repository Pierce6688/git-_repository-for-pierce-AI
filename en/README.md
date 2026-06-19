# TWSE Top 20 Stocks: Event-Driven Analysis of 10-Day Top 10 Gainers (As of 2026/06/16 Close) — English Translation

> **Generated**: 2026-06-17 15:10 (local time)
> **Statistics Cutoff**: 2026-06-16 after close (TWSE + TPEx)
> **Sample**: Electronics Sector Top 10 (Gain: +43.44% ~ +70.07%) + Financial Sector Top 10 (Gain: +10.02% ~ +26.92%)
> **Event Window**: 2026/05/15 ~ 2026/06/16 (covers 14 days before the base date 06/02 through the cutoff date, 33 days total)
> **Total Events**: 209 entries (149 individual stock + 60 macro/sector, original count) / 223 entries (events_by_company annotated)
> **Primary Data Sources**: Google News RSS aggregation of public media — Anue (cnyes), MoneyDJ, Economic Daily News, UDN, Yahoo Finance TW, CMoney, Sinotrade (sinotrade), Liberty Times Finance, Business Today, ETtoday Finance, TTV Global, Central News Agency (CNA), Economic Daily News

## What Is This

This is an **event-driven** analysis package covering 20 TWSE/TPEx stocks. It is **not** a stock pick recommendation, **not** a prediction, and **not** investment advice.

Its purpose is to:

- Map the 20 electronics/financial stocks with the highest 10-day gains onto an **event timeline**;
- Allow readers to see "**why they went up**" (sector catalysts, orders, revenue, shareholders' meetings, trading halts, etc.);
- Present the same data from **multiple perspectives**: HTML dashboard, Markdown summary tables, per-stock event logs, JSON for programmatic use, and SMA trend charts.

## File Inventory

| File | Type | Purpose |
|---|---|---|
| `index.html` | Web | Entry dashboard — open in any browser (double-click) |
| `report.md` | Markdown | Summary: Electronics/Financial Top 10 tables + 5-day details |
| `events_report.md` | Markdown | Full 209-event master table (chronological) |
| `events_by_company.md` | Markdown | Per-stock event timeline (20 stocks, one section each) |
| `2026-06-17_close_note.md` | Markdown | 6/17 closing flash note (continuation of the 6/16 report) |
| `all_events.json` | JSON | All events (including narrative paragraphs for 5/15~5/24) |
| `events_for_popup.json` | JSON | 20 individual stock events for frontend hover popups |
| `top10_returns.json` | JSON | Machine-readable Top 10 gains + 5-day details |
| `sector_lists.json` | JSON | Electronics/Financial sector stock lists |
| `tech_indicators.json` | JSON | Technical indicators: SMA5 / SMA20 / volume, etc. |
| `charts_ma/*.png` | PNG (5 files) | Sector moving average comparison charts |

## How to Use

1. **Start with `index.html`** (open in a browser): Electronics/Financial Top 10 tables, individual stock event tickers, and SMA trend charts.
2. **Looking for a specific company**: Go to `events_by_company.md` and Ctrl+F for the stock ticker (e.g., `2493`, `2883`).
3. **Want to see what happened on the timeline**: Scroll through `events_report.md` from start to finish.
4. **For programmatic access / further analysis**: All JSON files have complete schemas.

## Data Sources (each event is individually attributed in events_report.md)

Anue (cnyes) · MoneyDJ · Economic Daily News · Commercial Times · Liberty Times Finance · Central News Agency (CNA) · Focus Taiwan · ETtoday Finance · Yahoo Finance TW · CMoney · Sinotrade (sinotrade) · Business Today · TTV Global · UDN · UDN Money · Storm Media · RFI · TechNews · TradingKey · Economic Daily News

## Continuation After 6/17

- The 6/17 closing flash note is documented in `2026-06-17_close_note.md` (1 entry from Focus Taiwan: 45,877.39, +0.15%).
- 6/18 FOMC decision, 6/19 Taiwan Central Bank monetary policy meeting, 6/20 TSMC ex-dividend — see the "Key Watch Items for the Next 48 Hours" section in `2026-06-17_close_note.md` (calendar reminders only, **not predictions**).

## Known Limitations

- **Events before 5/15 are not covered**: By design, 5/15 is the starting point; macro context prior to 5/15 is not included.
- **Event counts reflect "media reports"**, not daily reconciliation with official company announcements: media coverage may lag, paraphrase, or consolidate multi-day events.
- **6/17 has only 1 post-close flash update**: the 20 stocks were not re-run for same-day price data and event scraping (limited by web_search tool unavailability; external media sites blocked by CloudFront/Datadome).
- **No individual stock recommendations**; all gain rankings are "post-hoc observations," not "stock picks."

## Disclaimer

- This archive is for research, documentation, and review purposes only; it is **not investment advice and not a stock recommendation**.
- All event attributions should be verified against original media sources; any media paraphrasing errors are not the responsibility of this archive.
- Investment decisions are made at your own risk and independent judgment.

## License & Sharing

- All data sources are from publicly available news, quoted under fair use principles with summaries and links.
- If redistributing this archive, please retain this README and source attributions.

---

*This is the English translation of the original Chinese-language report. All numeric data, dates, prices, and stock ticker codes are preserved exactly as in the source.*
