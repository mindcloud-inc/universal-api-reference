# <img src="https://images.mindcloud.co/apps/icons/refrens-icon_1778179792123.png" alt="Refrens logo" width="28" height="28"> Refrens: Universal API

Refrens is an invoicing and business finance platform. Its API supports creating business entities, invoices, expenditures, invoice payments, and India e-invoice IRN generation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/refrens/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.refrens.com/
- **Vendor API docs:** https://www.refrens.com/api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Token](actions/validate-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/validate-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Token](actions/create-token.md) | POST |  |
| [Validate Token](actions/validate-token.md) | GET |  |

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Create Business](actions/create-business.md) | POST |  |

### Expenditure

| Action | Method | Description |
| --- | --- | --- |
| [Create Expenditure](actions/create-expenditure.md) | POST |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Invoice](actions/cancel-invoice.md) | PUT |  |
| [Create Invoice](actions/create-invoice.md) | POST |  |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Invoice Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Invoice Email](actions/send-invoice-email.md) | POST |  |

### Invoice Irn

| Action | Method | Description |
| --- | --- | --- |
| [Generate Invoice IRN](actions/generate-invoice-irn.md) | POST |  |

### Invoice Payment

| Action | Method | Description |
| --- | --- | --- |
| [Add Invoice Payment](actions/add-invoice-payment.md) | POST |  |
| [List Invoice Payments](actions/list-invoice-payments.md) | GET |  |

