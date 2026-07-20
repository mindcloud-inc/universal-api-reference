# <img src="https://images.mindcloud.co/apps/icons/tidely_1774874580974.png" alt="Tidely logo" width="28" height="28"> Tidely: Universal API

Tidely helps businesses manage liquidity planning, cash flow forecasting, invoices, categories, scenarios, and plan values. This app wraps Tidely's public Open API for invoices and planning data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tidely/latest
- **Category:** Commerce / Accounting
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tidely.com
- **Vendor API docs:** https://faq.tidely.com/de/api-rechnungen

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Connection](actions/check-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tidely/latest/actions/check-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Budgets

| Action | Method | Description |
| --- | --- | --- |
| [Add To Existing Period Plan](actions/add-to-existing-period-plan.md) | POST |  |
| [Create Base Scenario Plan](actions/create-base-scenario-plan.md) | POST |  |
| [Create Daily Plan](actions/create-daily-plan.md) | POST |  |
| [Create Daily Plans In Bulk](actions/create-daily-plans-in-bulk.md) | POST |  |
| [Create Monthly Plan](actions/create-monthly-plan.md) | POST |  |
| [Create Monthly Plans In Bulk](actions/create-monthly-plans-in-bulk.md) | POST |  |
| [Create Plan](actions/create-plan.md) | POST |  |
| [Create Plans In Bulk](actions/create-plans-in-bulk.md) | POST |  |
| [Create Scenario Plan](actions/create-scenario-plan.md) | POST |  |
| [Create Weekly Plan](actions/create-weekly-plan.md) | POST |  |
| [Create Weekly Plans In Bulk](actions/create-weekly-plans-in-bulk.md) | POST |  |
| [Delete Category Plans In Scenario](actions/delete-category-plans-in-scenario.md) | DELETE |  |
| [Delete Plans](actions/delete-plans.md) | DELETE |  |
| [Replace Period Plan](actions/replace-period-plan.md) | POST |  |
| [Reset Scenario Plans For Category](actions/reset-scenario-plans-for-category.md) | DELETE |  |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories For Planned Transactions](actions/list-categories-for-planned-transactions.md) | GET |  |
| [List Expense Categories](actions/list-expense-categories.md) | GET |  |
| [List Income Categories](actions/list-income-categories.md) | GET |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Check Connection](actions/check-connection.md) | GET |  |

### Credit Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Sales Credit Note](actions/create-sales-credit-note.md) | POST |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Create Purchase Invoice](actions/create-purchase-invoice.md) | POST |  |
| [Create Sales Invoice](actions/create-sales-invoice.md) | POST |  |
| [Delete Invoice](actions/delete-invoice.md) | DELETE |  |
| [Mark Invoice Paid](actions/mark-invoice-paid.md) | PUT |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |
| [Void Invoice](actions/void-invoice.md) | PUT |  |

### Vendor Credits

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Credit Note](actions/create-purchase-credit-note.md) | POST |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Get Scenario](actions/get-scenario.md) | GET |  |
| [List Base Scenarios](actions/list-base-scenarios.md) | GET |  |
| [List Scenarios](actions/list-scenarios.md) | GET |  |

