# <img src="https://images.mindcloud.co/apps/icons/catalog-machine_1775149990187.png" alt="Catalog Machine logo" width="28" height="28"> Catalog Machine: Universal API

Catalog Machine helps teams manage product catalogs and automate product, order, and catalog workflows via REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/catalogMachine/latest
- **Category:** Commerce
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.catalogmachine.com
- **Vendor API docs:** https://help.catalogmachine.com/en/collections/1889860-automation-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Catalog

| Action | Method | Description |
| --- | --- | --- |
| [List Catalogs](actions/list-catalogs.md) | GET | Retrieves all catalogs from Catalog Machine. |
| [Rebuild Catalog PDF](actions/rebuild-catalog-pdf.md) | POST | Starts a catalog PDF rebuild job in Catalog Machine. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves all categories from Catalog Machine. |

### Csv

| Action | Method | Description |
| --- | --- | --- |
| [Import CSV Content](actions/import-csv-content.md) | POST | Starts a CSV import job in Catalog Machine. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Import Job Status](actions/get-import-job-status.md) | GET | Retrieves import job status from Catalog Machine. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [List Orders](actions/list-orders.md) | GET | Retrieves all orders from Catalog Machine. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes a product from Catalog Machine. |
| [Delete Products (Bulk)](actions/delete-products-bulk.md) | DELETE | Deletes multiple products from Catalog Machine. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product by code from Catalog Machine. |
| [List Products](actions/list-products.md) | GET | Retrieves all products from Catalog Machine. |
| [Upsert Product](actions/upsert-product.md) | PUT | Creates or updates a product in Catalog Machine. |
| [Upsert Products (Bulk)](actions/upsert-products-bulk.md) | PUT | Creates or updates multiple products in Catalog Machine. |

### Shopify

| Action | Method | Description |
| --- | --- | --- |
| [Start Shopify Import](actions/start-shopify-import.md) | POST | Starts a Shopify import job in Catalog Machine. |

