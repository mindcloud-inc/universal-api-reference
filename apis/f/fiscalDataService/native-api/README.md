# Fiscal Data Service: Native API Reference

A consolidated summary of Fiscal Data Service's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://fiscaldata.treasury.gov/api-documentation/
- **API base URL:** `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`

## Authentication

### No Authentication

Fiscal Data Service is a public API and does not require an account, API key, or token.

This API does not require request authentication.

[Official authentication documentation](https://fiscaldata.treasury.gov/api-documentation/)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Optional comma-separated Fiscal Data field names to include in the response. |
| `filter` | query | `string` | no | Optional Fiscal Data filter expression, such as record_date:gte:2024-01-01. |

Responses from this API use JSON. The total page count is read from `meta.total-pages`.

## Pagination

Use `page[size]` in the query string to set the page size (default 100; accepted range 1–1000). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Use `ascending` for ascending order and `-` for descending order. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Average Interest Rate Records](actions/list-average-interest-rate-records.md) | `GET /v2/accounting/od/avg_interest_rates` | [docs](https://fiscaldata.treasury.gov/datasets/average-interest-rates-treasury-securities/) |
| [List Daily Debt Subject to Limit Records](actions/list-daily-debt-subject-to-limit-records.md) | `GET /v1/accounting/dts/debt_subject_to_limit` | [docs](https://fiscaldata.treasury.gov/datasets/daily-treasury-statement/) |
| [List Daily Federal Tax Deposit Records](actions/list-daily-federal-tax-deposit-records.md) | `GET /v1/accounting/dts/federal_tax_deposits` | [docs](https://fiscaldata.treasury.gov/datasets/daily-treasury-statement/) |
| [List Daily Public Debt Transactions](actions/list-daily-public-debt-transactions.md) | `GET /v1/accounting/dts/public_debt_transactions` | [docs](https://fiscaldata.treasury.gov/datasets/daily-treasury-statement/) |
| [List Daily Treasury Deposits and Withdrawals](actions/list-daily-treasury-deposits-and-withdrawals.md) | `GET /v1/accounting/dts/deposits_withdrawals_operating_cash` | [docs](https://fiscaldata.treasury.gov/datasets/daily-treasury-statement/) |
| [List Daily Treasury Operating Cash Balances](actions/list-daily-treasury-operating-cash-balances.md) | `GET /v1/accounting/dts/operating_cash_balance` | [docs](https://fiscaldata.treasury.gov/datasets/daily-treasury-statement/) |
| [List Debt to the Penny Records](actions/list-debt-to-the-penny-records.md) | `GET /v2/accounting/od/debt_to_penny` | [docs](https://fiscaldata.treasury.gov/datasets/debt-to-the-penny/) |
| [List Electronic Securities Sales](actions/list-electronic-securities-sales.md) | `GET /v1/accounting/od/securities_sales` | [docs](https://fiscaldata.treasury.gov/datasets/electronic-securities-transactions/) |
| [List Government Revenue Collections](actions/list-government-revenue-collections.md) | `GET /v2/revenue/rcm` | [docs](https://fiscaldata.treasury.gov/datasets/revenue-collections-management/) |
| [List Historical Debt Outstanding Records](actions/list-historical-debt-outstanding-records.md) | `GET /v2/accounting/od/debt_outstanding` | [docs](https://fiscaldata.treasury.gov/datasets/historical-debt-outstanding/) |
| [List Monthly Public Debt Summary Records](actions/list-monthly-public-debt-summary-records.md) | `GET /v1/debt/mspd/mspd_table_1` | [docs](https://fiscaldata.treasury.gov/datasets/monthly-statement-public-debt/) |
| [List Monthly Receipts Outlays Deficit Surplus](actions/list-monthly-receipts-outlays-deficit-surplus.md) | `GET /v1/accounting/mts/mts_receipts_outlays_deficit_surplus` | [docs](https://fiscaldata.treasury.gov/datasets/monthly-treasury-statement/) |
| [List Monthly Statutory Debt Limit Records](actions/list-monthly-statutory-debt-limit-records.md) | `GET /v1/debt/mspd/mspd_table_2` | [docs](https://fiscaldata.treasury.gov/datasets/monthly-statement-public-debt/) |
| [List Monthly Treasury Outlays](actions/list-monthly-treasury-outlays.md) | `GET /v1/accounting/mts/mts_table_5` | [docs](https://fiscaldata.treasury.gov/datasets/monthly-treasury-statement/) |
| [List Monthly Treasury Receipts](actions/list-monthly-treasury-receipts.md) | `GET /v1/accounting/mts/mts_table_4` | [docs](https://fiscaldata.treasury.gov/datasets/monthly-treasury-statement/) |
| [List Monthly Treasury Security Detail Records](actions/list-monthly-treasury-security-detail-records.md) | `GET /v1/debt/mspd/mspd_table_3` | [docs](https://fiscaldata.treasury.gov/datasets/monthly-statement-public-debt/) |
| [List Monthly Treasury Statement Summary Records](actions/list-monthly-treasury-statement-summary-records.md) | `GET /v1/accounting/mts/mts_table_1` | [docs](https://fiscaldata.treasury.gov/datasets/monthly-treasury-statement/) |
| [List Public Debt Interest Expense Records](actions/list-public-debt-interest-expense-records.md) | `GET /v2/accounting/od/interest_expense` | [docs](https://fiscaldata.treasury.gov/datasets/interest-expense-debt-outstanding/) |
| [List Record Setting Auction Records](actions/list-record-setting-auction-records.md) | `GET /v2/accounting/od/record_setting_auction` | [docs](https://fiscaldata.treasury.gov/datasets/record-setting-auction-data/) |
| [List SLGS Security Records](actions/list-slgs-security-records.md) | `GET /v1/accounting/od/slgs_securities` | [docs](https://fiscaldata.treasury.gov/datasets/slgs-securities/) |
| [List Title XII Advance Records](actions/list-title-xii-advance-records.md) | `GET /v2/accounting/od/title_xii` | [docs](https://fiscaldata.treasury.gov/datasets/ssa-title-xii-advance-activities/) |
| [List Treasury Exchange Rates](actions/list-treasury-exchange-rates.md) | `GET /v1/accounting/od/rates_of_exchange` | [docs](https://fiscaldata.treasury.gov/datasets/treasury-reporting-rates-exchange/) |
| [List Treasury Gold Reserve Records](actions/list-treasury-gold-reserve-records.md) | `GET /v2/accounting/od/gold_reserve` | [docs](https://fiscaldata.treasury.gov/datasets/status-report-government-gold-reserve/) |
| [List Treasury Receivables Records](actions/list-treasury-receivables-records.md) | `GET /v2/debt/tror` | [docs](https://fiscaldata.treasury.gov/datasets/treasury-report-on-receivables/) |
