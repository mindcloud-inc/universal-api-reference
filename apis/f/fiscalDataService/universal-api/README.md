# Fiscal Data Service: Universal API

Access public U.S. Treasury Fiscal Data APIs for federal debt, cash balances, receipts, outlays, revenue collections, exchange rates, interest costs, securities, and related fiscal datasets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fiscalDataService/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fiscaldata.treasury.gov/
- **Vendor API docs:** https://fiscaldata.treasury.gov/api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Debt to the Penny Records](actions/list-debt-to-the-penny-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-debt-to-the-penny-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Average Interest Rate Record

| Action | Method | Description |
| --- | --- | --- |
| [List Average Interest Rate Records](actions/list-average-interest-rate-records.md) | GET | Retrieves average interest rate records from Fiscal Data Service. |

### Debt Subject To Limit Record

| Action | Method | Description |
| --- | --- | --- |
| [List Daily Debt Subject to Limit Records](actions/list-daily-debt-subject-to-limit-records.md) | GET | Retrieves daily debt subject to limit records from Fiscal Data Service. |

### Debt To The Penny Record

| Action | Method | Description |
| --- | --- | --- |
| [List Debt to the Penny Records](actions/list-debt-to-the-penny-records.md) | GET | Retrieves Debt to the Penny records from Fiscal Data Service. |

### Electronic Securities Sale

| Action | Method | Description |
| --- | --- | --- |
| [List Electronic Securities Sales](actions/list-electronic-securities-sales.md) | GET | Retrieves electronic securities sales from Fiscal Data Service. |

### Federal Tax Deposit Record

| Action | Method | Description |
| --- | --- | --- |
| [List Daily Federal Tax Deposit Records](actions/list-daily-federal-tax-deposit-records.md) | GET | Retrieves daily federal tax deposit records from Fiscal Data Service. |

### Government Revenue Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Government Revenue Collections](actions/list-government-revenue-collections.md) | GET | Retrieves government revenue collections from Fiscal Data Service. |

### Historical Debt Outstanding Record

| Action | Method | Description |
| --- | --- | --- |
| [List Historical Debt Outstanding Records](actions/list-historical-debt-outstanding-records.md) | GET | Retrieves historical debt outstanding records from Fiscal Data Service. |

### Monthly Fiscal Summary Amount

| Action | Method | Description |
| --- | --- | --- |
| [List Monthly Receipts Outlays Deficit Surplus](actions/list-monthly-receipts-outlays-deficit-surplus.md) | GET | Retrieves monthly receipts and outlays records from Fiscal Data Service. |

### Monthly Public Debt Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Monthly Public Debt Summary Records](actions/list-monthly-public-debt-summary-records.md) | GET | Retrieves monthly public debt summary records from Fiscal Data Service. |

### Monthly Treasury Outlay

| Action | Method | Description |
| --- | --- | --- |
| [List Monthly Treasury Outlays](actions/list-monthly-treasury-outlays.md) | GET | Retrieves monthly Treasury outlays from Fiscal Data Service. |

### Monthly Treasury Receipt

| Action | Method | Description |
| --- | --- | --- |
| [List Monthly Treasury Receipts](actions/list-monthly-treasury-receipts.md) | GET | Retrieves monthly Treasury receipts from Fiscal Data Service. |

### Monthly Treasury Statement Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Monthly Treasury Statement Summary Records](actions/list-monthly-treasury-statement-summary-records.md) | GET | Retrieves monthly Treasury statement summary records from Fiscal Data Service. |

### Operating Cash Balance

| Action | Method | Description |
| --- | --- | --- |
| [List Daily Treasury Operating Cash Balances](actions/list-daily-treasury-operating-cash-balances.md) | GET | Retrieves daily Treasury operating cash balances from Fiscal Data Service. |

### Public Debt Interest Expense Record

| Action | Method | Description |
| --- | --- | --- |
| [List Public Debt Interest Expense Records](actions/list-public-debt-interest-expense-records.md) | GET | Retrieves public debt interest expense records from Fiscal Data Service. |

### Public Debt Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Daily Public Debt Transactions](actions/list-daily-public-debt-transactions.md) | GET | Retrieves daily public debt transactions from Fiscal Data Service. |

### Record Setting Auction Record

| Action | Method | Description |
| --- | --- | --- |
| [List Record Setting Auction Records](actions/list-record-setting-auction-records.md) | GET | Retrieves record-setting auction records from Fiscal Data Service. |

### Slgs Security Record

| Action | Method | Description |
| --- | --- | --- |
| [List SLGS Security Records](actions/list-slgs-security-records.md) | GET | Retrieves SLGS security records from Fiscal Data Service. |

### Statutory Debt Limit Record

| Action | Method | Description |
| --- | --- | --- |
| [List Monthly Statutory Debt Limit Records](actions/list-monthly-statutory-debt-limit-records.md) | GET | Retrieves monthly statutory debt limit records from Fiscal Data Service. |

### Title Xii Advance Record

| Action | Method | Description |
| --- | --- | --- |
| [List Title XII Advance Records](actions/list-title-xii-advance-records.md) | GET | Retrieves Title XII advance records from Fiscal Data Service. |

### Treasury Deposit Or Withdrawal

| Action | Method | Description |
| --- | --- | --- |
| [List Daily Treasury Deposits and Withdrawals](actions/list-daily-treasury-deposits-and-withdrawals.md) | GET | Retrieves daily Treasury deposits and withdrawals from Fiscal Data Service. |

### Treasury Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [List Treasury Exchange Rates](actions/list-treasury-exchange-rates.md) | GET | Retrieves Treasury exchange rates from Fiscal Data Service. |

### Treasury Gold Reserve Record

| Action | Method | Description |
| --- | --- | --- |
| [List Treasury Gold Reserve Records](actions/list-treasury-gold-reserve-records.md) | GET | Retrieves Treasury gold reserve records from Fiscal Data Service. |

### Treasury Receivable Record

| Action | Method | Description |
| --- | --- | --- |
| [List Treasury Receivables Records](actions/list-treasury-receivables-records.md) | GET | Retrieves Treasury receivables records from Fiscal Data Service. |

### Treasury Security Detail Record

| Action | Method | Description |
| --- | --- | --- |
| [List Monthly Treasury Security Detail Records](actions/list-monthly-treasury-security-detail-records.md) | GET | Retrieves monthly Treasury security detail records from Fiscal Data Service. |

