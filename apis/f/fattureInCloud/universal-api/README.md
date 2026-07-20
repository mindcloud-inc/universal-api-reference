# <img src="https://images.mindcloud.co/apps/icons/elegant-ts-logo-in-vibrant-gradients_1775577017243.png" alt="Fatture in Cloud logo" width="28" height="28"> Fatture in Cloud: Universal API

Manage invoices, clients, products, and accounting documents

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fattureInCloud/latest
- **Category:** Commerce / Accounting
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fattureincloud.it
- **Vendor API docs:** https://developers.fattureincloud.it/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List User Companies](actions/list-user-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-user-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Info](actions/get-company-info.md) | GET | Retrieves company info from Fatture in Cloud. |
| [List User Companies](actions/list-user-companies.md) | GET | Retrieves the user's companies from Fatture in Cloud. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Fatture in Cloud. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Fatture in Cloud. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Fatture in Cloud. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Fatture in Cloud. |
| [Modify Client](actions/modify-client.md) | PUT | Updates an existing client in Fatture in Cloud. |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [Create Received Document](actions/create-received-document.md) | POST | Creates a new received document in Fatture in Cloud. |
| [Delete Received Document](actions/delete-received-document.md) | DELETE | Deletes an existing received document from Fatture in Cloud. |
| [Get Received Document](actions/get-received-document.md) | GET | Retrieves a received document from Fatture in Cloud. |
| [List Received Documents](actions/list-received-documents.md) | GET | Retrieves received documents from Fatture in Cloud. |
| [Modify Received Document](actions/modify-received-document.md) | PUT | Updates an existing received document in Fatture in Cloud. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Issued Document](actions/create-issued-document.md) | POST | Creates a new issued document in Fatture in Cloud. |
| [Delete Issued Document](actions/delete-issued-document.md) | DELETE | Deletes an existing issued document from Fatture in Cloud. |
| [Get Issued Document](actions/get-issued-document.md) | GET | Retrieves an issued document from Fatture in Cloud. |
| [List Issued Documents](actions/list-issued-documents.md) | GET | Retrieves issued documents from Fatture in Cloud. |
| [Modify Issued Document](actions/modify-issued-document.md) | PUT | Updates an existing issued document in Fatture in Cloud. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Receipt](actions/create-receipt.md) | POST | Creates a new receipt in Fatture in Cloud. |
| [Get Receipt](actions/get-receipt.md) | GET | Retrieves a receipt from Fatture in Cloud. |
| [List Receipts](actions/list-receipts.md) | GET | Retrieves receipts from Fatture in Cloud. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Fatture in Cloud. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Fatture in Cloud. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Fatture in Cloud. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Fatture in Cloud. |
| [Modify Product](actions/modify-product.md) | PUT | Updates an existing product in Fatture in Cloud. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST | Creates a new supplier in Fatture in Cloud. |
| [Delete Supplier](actions/delete-supplier.md) | DELETE | Deletes an existing supplier from Fatture in Cloud. |
| [Get Supplier](actions/get-supplier.md) | GET | Retrieves a supplier from Fatture in Cloud. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves suppliers from Fatture in Cloud. |
| [Modify Supplier](actions/modify-supplier.md) | PUT | Updates an existing supplier in Fatture in Cloud. |

