# <img src="https://images.mindcloud.co/apps/icons/781d2f73faf9be2779ba6c641fbbb782_1775166078167.png" alt="Zoho Books logo" width="28" height="28"> Zoho Books: Universal API

Manage invoices, expenses, taxes, reconciliation, and financial reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoBooks/latest
- **Category:** Commerce / Accounting
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/books/
- **Vendor API docs:** https://www.zoho.com/books/api/v3/introduction/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [Create Bill](actions/create-bill.md) | POST |  |
| [Get Bill](actions/get-bill.md) | GET |  |
| [List Bills](actions/list-bills.md) | GET |  |
| [Update Bill](actions/update-bill.md) | PUT |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Customer Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Payment](actions/create-customer-payment.md) | POST |  |
| [List Customer Payments](actions/list-customer-payments.md) | GET |  |
| [Retrieve Customer Payment](actions/retrieve-customer-payment.md) | GET |  |
| [Update Customer Payment](actions/update-customer-payment.md) | PUT |  |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST |  |
| [Get Estimate](actions/get-estimate.md) | GET |  |
| [List Estimates](actions/list-estimates.md) | GET |  |
| [Update Estimate](actions/update-estimate.md) | PUT |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [Update Invoice](actions/update-invoice.md) | PUT |  |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST |  |
| [Get Item](actions/get-item.md) | GET |  |
| [List Items](actions/list-items.md) | GET |  |
| [Update Item](actions/update-item.md) | PUT |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET |  |

