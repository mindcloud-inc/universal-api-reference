# <img src="https://images.mindcloud.co/apps/icons/joiin_1774894087446.png" alt="Joiin logo" width="28" height="28"> Joiin: Universal API

Manage companies and generate consolidated financial reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/joiin/latest
- **Category:** Commerce / Accounting
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.joiin.co/
- **Vendor API docs:** https://app.joiin.co/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Companies](actions/list-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joiin/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Balance Sheet Report

| Action | Method | Description |
| --- | --- | --- |
| [Run Balance Sheet Report](actions/run-balance-sheet-report.md) | GET | Retrieves a balance sheet report from Joiin. |

### Cashflow Report

| Action | Method | Description |
| --- | --- | --- |
| [Run Cashflow Report](actions/run-cashflow-report.md) | GET | Retrieves a cashflow report from Joiin. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | POST | Creates a company in Joiin. |
| [Delete Company](actions/delete-company.md) | DELETE | Deletes an existing company from Joiin. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from Joiin. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in Joiin. |

### Custom Report

| Action | Method | Description |
| --- | --- | --- |
| [Run Custom Report](actions/run-custom-report.md) | GET | Retrieves a custom report from Joiin. |

### Profit And Loss Report

| Action | Method | Description |
| --- | --- | --- |
| [Run Profit and Loss Report](actions/run-profit-and-loss-report.md) | GET | Retrieves a profit and loss report from Joiin. |

### Trial Balance Report

| Action | Method | Description |
| --- | --- | --- |
| [Run Trial Balance Report](actions/run-trial-balance-report.md) | GET | Retrieves a trial balance report from Joiin. |

