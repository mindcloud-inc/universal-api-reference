# <img src="https://images.mindcloud.co/apps/icons/apple-touch-icon_1782233203690.png" alt="Sage Intacct logo" width="28" height="28"> Sage Intacct: Universal API

Sage Intacct through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/intacct/latest
- **Category:** Commerce / Accounting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sage.com/en-us/sage-business-cloud/intacct/
- **Vendor API docs:** https://developer.intacct.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check GLBATCH Duplicate](actions/check-glbatch-duplicate.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/check-glbatch-duplicate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Bills

| Action | Method | Description |
| --- | --- | --- |
| [Create Bill Item](actions/createbillitem.md) | POST |  |

### Budgets

| Action | Method | Description |
| --- | --- | --- |
| [Create Budget](actions/create-budget.md) | POST |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts](actions/list-contacts.md) | GET |  |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Fields for Object](actions/get-fields.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST |  |

### General Ledger Batch

| Action | Method | Description |
| --- | --- | --- |
| [Check GLBATCH Duplicate](actions/check-glbatch-duplicate.md) | GET |  |
| [Create Journal](actions/createjournal.md) | POST |  |
| [Update Journal](actions/update-journal.md) | PUT |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Create Sales Invoice](actions/create-sales-invoice.md) | POST |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST |  |
| [Create Item New](actions/create-item-2.md) | POST |  |
| [Get Custom Object](actions/get-custom-object.md) | GET |  |
| [Get Full Item](actions/get-full-item.md) | GET |  |
| [Get Full Item By Name](actions/get-full-item-by-name.md) | GET |  |
| [Update Item](actions/update-item.md) | PUT |  |

### Order Entry Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create So Transaction](actions/create-so-transaction.md) | POST |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Post Raw to Stripe](actions/post-raw-to-stripe.md) | POST |  |
| [Read Bank Deposits](actions/read-bank-deposits.md) | POST |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Query Object](actions/query-object.md) | GET |  |
| [Query Object Sum](actions/query-object-sum.md) | GET |  |
| [Read By Query](actions/read-by-query.md) | GET |  |

