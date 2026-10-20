STOCK MARKET CONTROL TOWER — UPDATED DATASET PACKAGE

Added:
- 18_portfolio.csv: synthetic portfolio master with one portfolio per client from Client Master.
  It has portfolio_id, client_id, portfolio_name, portfolio_type, base_currency,
  created_date, portfolio_status, as_of_date.
  Important: portfolio_id mappings are newly generated for project modeling; they were not present in the original source data.
  This file is a portfolio MASTER / client-to-portfolio mapping, not a source of portfolio valuation or P&L.
  Valuation and P&L must be calculated from holdings, positions, transactions, prices, charges and dividends.

Other additions already present in the uploaded package include transaction ledger, settlement cash ledger,
risk-free rates, enriched instrument master, sector mapping, quote-enriched tick data, and trade-level quotes.

Coverage:
- See REQUIREMENT_COVERAGE.csv for part-by-part alignment with the 13 project sections.
- See DATASET_QUALITY_SUMMARY.csv for row counts, duplicate-row counts and missing cells.
- See DATA_VALIDATION_CHECKS.csv for basic key/link validation.

Important limitations:
- The core 14 datasets are present, plus supporting/enriched files and the new portfolio master.
- A portfolio master alone does not create a dated portfolio valuation series.
- Historical holdings and positions snapshots run from 2026-09-08 to 2026-10-05 (20 dates).
- Current holdings and positions snapshots are dated 2026-10-05.
- Historical OHLCV spans 2025-10-21 to 2026-10-05 (250 dates); tick data spans 2026-09-29 to 2026-10-05.
- Corporate-action reconciliation requires explicit split/bonus/symbol-change adjustment logic.
- Check missing values and null meanings before cleaning; not every null is invalid (e.g. failure_reason when settlement succeeded).
