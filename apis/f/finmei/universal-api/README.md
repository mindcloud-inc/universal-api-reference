# <img src="https://images.mindcloud.co/apps/icons/finmei-icon_1775157084252.png" alt="Finmei logo" width="28" height="28"> Finmei: Universal API

Create invoices, track expenses, and manage business profile data in Finmei.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/finmei/latest
- **Category:** Commerce / Accounting
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.finmei.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Invoices](actions/list-invoices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmei/latest/actions/list-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Download Expense](actions/download-expense.md) | GET |  |
| [Download Invoice](actions/download-invoice.md) | GET |  |
| [Replace Expense File](actions/replace-expense-file.md) | PUT |  |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile](actions/get-profile.md) | GET |  |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST |  |
| [Delete Expense](actions/delete-expense.md) | DELETE |  |
| [Get Expense](actions/get-expense.md) | GET |  |
| [List Expenses](actions/list-expenses.md) | GET |  |
| [Patch Expense](actions/patch-expense.md) | PUT |  |
| [Update Expense](actions/update-expense.md) | PUT |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Delete Invoice](actions/delete-invoice.md) | DELETE |  |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [Patch Invoice](actions/patch-invoice.md) | PUT |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET |  |

