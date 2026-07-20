# <img src="https://images.mindcloud.co/apps/icons/favicon-developer-tiliter-com-48x48_1775855825085.png" alt="Tiliter logo" width="28" height="28"> Tiliter: Universal API

Tiliter Recognition API for stores, devices, products, mappings, stock, and recognition event reporting.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tiliter/latest
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tiliter.com
- **Vendor API docs:** https://developer.tiliter.com/reference/index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Health Check](actions/health-check.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Device](actions/create-device.md) | POST | Creates a device in the Tiliter Recognition API. |
| [Create Or Update Products Batch](actions/create-or-update-products-batch.md) | POST | Creates or updates products in Tiliter in a batch. |
| [Create Product](actions/create-product.md) | POST | Creates a product in the Tiliter Recognition API. |
| [Create Product Mapping](actions/create-product-mapping.md) | POST | Creates a product mapping in the Tiliter Recognition API. |
| [Create Product Sample](actions/create-product-sample.md) | POST | Creates a product sample in the Tiliter Recognition API. |
| [Create Recognition Request](actions/create-recognition-request.md) | POST | Creates a recognition request in the Tiliter Recognition API. |
| [Create Selection Report](actions/create-selection-report.md) | POST | Creates a selection report in the Tiliter Recognition API. |
| [Create Store](actions/create-store.md) | POST | Creates a store in the Tiliter Recognition API. |
| [Create Transaction Event](actions/create-transaction-event.md) | POST | Creates a transaction event in the Tiliter Recognition API. |
| [Create Transaction Events Batch](actions/create-transaction-events-batch.md) | POST | Creates transaction events in Tiliter in a batch. |
| [Delete Device](actions/delete-device.md) | DELETE | Deletes a device from the Tiliter Recognition API. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes a product from the Tiliter Recognition API. |
| [Delete Product Mapping](actions/delete-product-mapping.md) | DELETE | Deletes a product mapping from the Tiliter Recognition API. |
| [Delete Product Sample](actions/delete-product-sample.md) | DELETE | Deletes a product sample from the Tiliter Recognition API. |
| [Delete Store](actions/delete-store.md) | DELETE | Deletes a store from the Tiliter Recognition API. |
| [Get Device](actions/get-device.md) | GET | Retrieves a device from the Tiliter Recognition API. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from the Tiliter Recognition API. |
| [Get Product Mapping](actions/get-product-mapping.md) | GET | Retrieves a product mapping from the Tiliter Recognition API. |
| [Get Product Sample](actions/get-product-sample.md) | GET | Retrieves a product sample from the Tiliter Recognition API. |
| [Get Store](actions/get-store.md) | GET | Retrieves a store from the Tiliter Recognition API. |
| [Get Store Stock](actions/get-store-stock.md) | GET | Retrieves store stock from the Tiliter Recognition API. |
| [Health Check](actions/health-check.md) | GET | Retrieves the Tiliter Recognition API health status. |
| [List Archetypes](actions/list-archetypes.md) | GET | Retrieves archetypes from the Tiliter Recognition API. |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices from the Tiliter Recognition API. |
| [List Product Mappings](actions/list-product-mappings.md) | GET | Retrieves product mappings from the Tiliter Recognition API. |
| [List Products](actions/list-products.md) | GET | Retrieves products from the Tiliter Recognition API. |
| [List Stores](actions/list-stores.md) | GET | Retrieves stores from the Tiliter Recognition API. |
| [Update Device](actions/update-device.md) | PUT | Updates a device in the Tiliter Recognition API. |
| [Update Product](actions/update-product.md) | PUT | Updates a product in the Tiliter Recognition API. |
| [Update Product Mapping](actions/update-product-mapping.md) | PUT | Updates a product mapping in the Tiliter Recognition API. |
| [Update Store](actions/update-store.md) | PUT | Updates a store in the Tiliter Recognition API. |
| [Update Store Stock](actions/update-store-stock.md) | PUT | Updates store stock in the Tiliter Recognition API. |

