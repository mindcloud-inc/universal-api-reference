# <img src="https://images.mindcloud.co/apps/icons/b2b-bigcommerce_1753305366940.png" alt="BigCommerce (B2B) logo" width="28" height="28"> BigCommerce (B2B): Universal API

BigCommerce (B2B) through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bigCommerceB2B/latest
- **Category:** Commerce
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.bigcommerce.com/b2b-edition
- **Vendor API docs:** https://developer.bigcommerce.com/b2b-edition/apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get invoices](actions/get-invoices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get All Companies](actions/get-all-companies.md) | GET |  |
| [Get Company](actions/get-company.md) | GET |  |
| [Get Company Credit](actions/get-company-credit.md) | GET |  |
| [Get Company Payment Methods](actions/get-company-payment-methods.md) | PUT |  |
| [Get Company Payment Terms](actions/get-company-payment-terms.md) | PUT |  |
| [Update Company](actions/update-company.md) | PUT |  |
| [Update Company Credit](actions/update-company-credit.md) | PUT |  |
| [Update Company Payment Methods](actions/update-company-payment-methods.md) | PUT |  |
| [Update Company Payment Terms](actions/update-company-payment-terms.md) | PUT |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [Get invoices](actions/get-invoices.md) | GET |  |
| [Update Invoice](actions/update-invoice.md) | POST |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET |  |

