# <img src="https://images.mindcloud.co/apps/icons/favicon_1773946710515.png" alt="Quaderno logo" width="28" height="28"> Quaderno: Universal API

Quaderno is tax compliance software that automates sales tax, VAT, and GST calculations, invoicing, and reporting for SaaS, ecommerce, and digital businesses worldwide.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quaderno/latest
- **Category:** Commerce / Accounting
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quaderno.io/
- **Vendor API docs:** https://developers.quaderno.io/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tax Codes](actions/list-tax-codes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quaderno/latest/actions/list-tax-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Quaderno. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Quaderno. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from Quaderno. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact record from Quaderno. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Quaderno. |

### Credit Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Credit Note](actions/create-credit-note.md) | POST | Creates a credit note for an invoice in Quaderno. |
| [List Credit Notes](actions/list-credit-notes.md) | GET | Retrieves credit notes from Quaderno. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Quaderno. |
| [Deliver Invoice](actions/deliver-invoice.md) | GET | Delivers an invoice to the customer by email in Quaderno. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Quaderno. |
| [Mark Invoice Uncollectible](actions/mark-invoice-uncollectible.md) | PUT | Marks an invoice as uncollectible in Quaderno. |
| [Retrieve Invoice](actions/retrieve-invoice.md) | GET | Retrieves an invoice from Quaderno. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Quaderno. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Record Invoice Payment](actions/record-invoice-payment.md) | POST | Records a payment for an invoice in Quaderno. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Quaderno. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Quaderno. |
| [List Products](actions/list-products.md) | GET | Retrieves product records from Quaderno. |
| [Retrieve Product](actions/retrieve-product.md) | GET | Retrieves a product record from Quaderno. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Quaderno. |

### Receipt

| Action | Method | Description |
| --- | --- | --- |
| [Create Receipt](actions/create-receipt.md) | POST | Creates a paid receipt in Quaderno. |
| [Deliver Receipt](actions/deliver-receipt.md) | GET | Delivers a receipt to the customer by email in Quaderno. |
| [List Receipts](actions/list-receipts.md) | GET | Retrieves receipts from Quaderno. |
| [Retrieve Receipt](actions/retrieve-receipt.md) | GET | Retrieves a receipt from Quaderno. |

### Recurring Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Recurring Document](actions/create-recurring-document.md) | POST | Creates a recurring billing document in Quaderno. |
| [List Recurring Documents](actions/list-recurring-documents.md) | GET | Retrieves recurring billing documents from Quaderno. |

### Tax Code

| Action | Method | Description |
| --- | --- | --- |
| [List Tax Codes](actions/list-tax-codes.md) | GET | Retrieves supported tax codes from Quaderno. |

### Tax Id

| Action | Method | Description |
| --- | --- | --- |
| [Create Tax ID](actions/create-tax-id.md) | POST | Creates a registered tax ID in Quaderno. |
| [List Tax IDs](actions/list-tax-ids.md) | GET | Retrieves registered tax IDs from Quaderno. |
| [Validate Tax ID](actions/validate-tax-id.md) | GET | Validates a tax ID in Quaderno. |

