# Fiscal Data Service Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Fiscal Data Service expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-average-interest-rate-records?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Fiscal Data Service actions that support pagination

- [List Average Interest Rate Records](actions/list-average-interest-rate-records.md)
- [List Daily Debt Subject to Limit Records](actions/list-daily-debt-subject-to-limit-records.md)
- [List Daily Federal Tax Deposit Records](actions/list-daily-federal-tax-deposit-records.md)
- [List Daily Public Debt Transactions](actions/list-daily-public-debt-transactions.md)
- [List Daily Treasury Deposits and Withdrawals](actions/list-daily-treasury-deposits-and-withdrawals.md)
- [List Daily Treasury Operating Cash Balances](actions/list-daily-treasury-operating-cash-balances.md)
- [List Debt to the Penny Records](actions/list-debt-to-the-penny-records.md)
- [List Electronic Securities Sales](actions/list-electronic-securities-sales.md)
- [List Government Revenue Collections](actions/list-government-revenue-collections.md)
- [List Historical Debt Outstanding Records](actions/list-historical-debt-outstanding-records.md)
- [List Monthly Public Debt Summary Records](actions/list-monthly-public-debt-summary-records.md)
- [List Monthly Receipts Outlays Deficit Surplus](actions/list-monthly-receipts-outlays-deficit-surplus.md)
- [List Monthly Statutory Debt Limit Records](actions/list-monthly-statutory-debt-limit-records.md)
- [List Monthly Treasury Outlays](actions/list-monthly-treasury-outlays.md)
- [List Monthly Treasury Receipts](actions/list-monthly-treasury-receipts.md)
- [List Monthly Treasury Security Detail Records](actions/list-monthly-treasury-security-detail-records.md)
- [List Monthly Treasury Statement Summary Records](actions/list-monthly-treasury-statement-summary-records.md)
- [List Public Debt Interest Expense Records](actions/list-public-debt-interest-expense-records.md)
- [List Record Setting Auction Records](actions/list-record-setting-auction-records.md)
- [List SLGS Security Records](actions/list-slgs-security-records.md)
- [List Title XII Advance Records](actions/list-title-xii-advance-records.md)
- [List Treasury Exchange Rates](actions/list-treasury-exchange-rates.md)
- [List Treasury Gold Reserve Records](actions/list-treasury-gold-reserve-records.md)
- [List Treasury Receivables Records](actions/list-treasury-receivables-records.md)
