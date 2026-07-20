# <img src="https://images.mindcloud.co/apps/icons/e-gestor_1775060627483.png" alt="eGestor logo" width="28" height="28"> eGestor: Universal API

Manage eGestor sales, purchases, inventory, finance, and invoices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eGestor/latest
- **Category:** Commerce / ERP
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://egestor.com.br/
- **Vendor API docs:** https://egestor.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Pix Status](actions/check-pix-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGestor/latest/actions/check-pix-status?connectionId=$CONNECTION_ID&codigo=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves company details from eGestor. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in eGestor. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from eGestor. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves details for a contact from eGestor. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from eGestor. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in eGestor. |

### Payable

| Action | Method | Description |
| --- | --- | --- |
| [Create Payable](actions/create-payable.md) | POST | Creates a new payable in eGestor. |
| [Get Payable](actions/get-payable.md) | GET | Retrieves details for a payable from eGestor. |
| [List Payables](actions/list-payables.md) | GET | Retrieves a list of payables from eGestor. |
| [Pay Payable](actions/pay-payable.md) | PUT | Marks a payable as paid in eGestor. |
| [Update Payable](actions/update-payable.md) | PUT | Updates an existing payable in eGestor. |

### Pix Charge

| Action | Method | Description |
| --- | --- | --- |
| [Check Pix Status](actions/check-pix-status.md) | GET | Retrieves the status of a Pix charge from eGestor. |
| [Create Pix Charge](actions/create-pix-charge.md) | POST | Creates a new Pix charge in eGestor. |
| [Get Pix Charge](actions/get-pix-charge.md) | GET | Retrieves details for a Pix charge from eGestor. |
| [List Pix Charges](actions/list-pix-charges.md) | GET | Retrieves a list of Pix charges from eGestor. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in eGestor. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from eGestor. |
| [Get Product](actions/get-product.md) | GET | Retrieves details for a product from eGestor. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from eGestor. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in eGestor. |

### Purchase

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase](actions/create-purchase.md) | POST | Creates a new purchase in eGestor. |
| [Finalize Purchase](actions/finalize-purchase.md) | PUT | Finalizes a purchase in eGestor. |
| [Get Purchase](actions/get-purchase.md) | GET | Retrieves details for a purchase from eGestor. |
| [List Purchases](actions/list-purchases.md) | GET | Retrieves a list of purchases from eGestor. |
| [Reopen Purchase](actions/reopen-purchase.md) | PUT | Reopens a purchase in eGestor. |

### Receivable

| Action | Method | Description |
| --- | --- | --- |
| [Create Receivable](actions/create-receivable.md) | POST | Creates a new receivable in eGestor. |
| [Get Receivable](actions/get-receivable.md) | GET | Retrieves details for a receivable from eGestor. |
| [List Receivables](actions/list-receivables.md) | GET | Retrieves a list of receivables from eGestor. |
| [Receive Receivable](actions/receive-receivable.md) | PUT | Marks a receivable as received in eGestor. |
| [Update Receivable](actions/update-receivable.md) | PUT | Updates an existing receivable in eGestor. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Create Sale](actions/create-sale.md) | POST | Creates a new sale in eGestor. |
| [Generate Sale NFe](actions/generate-sale-n-fe.md) | PUT | Generates an NFe for a sale in eGestor. |
| [Get Sale](actions/get-sale.md) | GET | Retrieves details for a sale from eGestor. |
| [List Sales](actions/list-sales.md) | GET | Retrieves a list of sales from eGestor. |
| [Update Sale](actions/update-sale.md) | PUT | Updates an existing sale in eGestor. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create Service](actions/create-service.md) | POST | Creates a new service in eGestor. |
| [Delete Service](actions/delete-service.md) | DELETE | Deletes an existing service from eGestor. |
| [Get Service](actions/get-service.md) | GET | Retrieves details for a service from eGestor. |
| [List Services](actions/list-services.md) | GET | Retrieves a list of services from eGestor. |
| [Update Service](actions/update-service.md) | PUT | Updates an existing service in eGestor. |

