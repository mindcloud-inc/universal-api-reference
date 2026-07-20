# <img src="https://images.mindcloud.co/apps/icons/gelato_1776722246671.png" alt="Gelato logo" width="28" height="28"> Gelato: Universal API

Gelato API integration

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gelato/latest
- **Category:** Commerce
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gelato.com/
- **Vendor API docs:** https://dashboard.gelato.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Catalogs](actions/list-catalogs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/list-catalogs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog](actions/get-catalog.md) | GET | Retrieves a product catalog from Gelato by ID. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [List Catalogs](actions/list-catalogs.md) | GET | Finds available product catalogs in Gelato. |

### Cover Dimensions

| Action | Method | Description |
| --- | --- | --- |
| [Cover Dimensions](actions/cover-dimensions.md) | GET | Retrieves cover dimensions for a Gelato product. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order v2](actions/cancel-order-v2.md) | PUT | Cancels an order in Gelato v2 by order reference ID. |
| [Cancel Order v3](actions/cancel-order-v3.md) | PUT | Cancels an order in Gelato v3. |
| [Cancel Order v4](actions/cancel-order-v4.md) | PUT | Cancels an order in Gelato v4. |
| [Create Order v2](actions/create-order-v2.md) | POST | Creates an order in Gelato v2 from a promise UID. |
| [Create Order v3](actions/create-order-v3.md) | POST | Creates an order in Gelato v3. |
| [Create Order v4](actions/create-order-v4.md) | POST | Creates an order in Gelato v4. |
| [Delete Draft Order v3](actions/delete-draft-order-v3.md) | DELETE | Deletes a draft order from Gelato v3. |
| [Delete Draft Order v4](actions/delete-draft-order-v4.md) | DELETE | Deletes a draft order from Gelato v4. |
| [Get Order Status v2](actions/get-order-status-v2.md) | GET | Retrieves order status details from Gelato v2. |
| [Get Order v3](actions/get-order-v3.md) | GET | Retrieves an order from Gelato v3. |
| [Get Order v4](actions/get-order-v4.md) | GET | Retrieves an order from Gelato v4. |
| [Get Shipping Address v2](actions/get-shipping-address-v2.md) | GET | Retrieves a shipping address for an order in Gelato v2. |
| [Get Shipping Address v3](actions/get-shipping-address-v3.md) | GET | Retrieves a shipping address for an order in Gelato v3. |
| [Patch Draft Order v3](actions/patch-draft-order-v3.md) | PUT | Converts a draft order into a regular order in Gelato v3. |
| [Patch Draft Order v4](actions/patch-draft-order-v4.md) | PUT | Converts a draft order into a regular order in Gelato v4. |
| [Update Shipping Address v2](actions/update-shipping-address-v2.md) | PUT | Updates an order shipping address in Gelato v2. |
| [Update Shipping Address v3](actions/update-shipping-address-v3.md) | PUT | Updates an order shipping address in Gelato v3. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Search Orders v3](actions/search-orders-v3.md) | GET | Finds orders in Gelato v3 by filters. |
| [Search Orders v4](actions/search-orders-v4.md) | GET | Finds orders in Gelato v4 by filters. |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [Price](actions/price.md) | GET | Retrieves product prices from Gelato by country and currency. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Gelato by ID. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Search Products](actions/search-products.md) | GET | Finds products in a Gelato catalog by attributes. |

### Quote

| Action | Method | Description |
| --- | --- | --- |
| [Quote Order v2](actions/quote-order-v2.md) | GET | Retrieves shipping options and promise UIDs in Gelato v2. |
| [Quote Order v3](actions/quote-order-v3.md) | GET | Retrieves shipping quotes for order items in Gelato v3. |
| [Quote Order v4](actions/quote-order-v4.md) | GET | Retrieves shipping quotes for order items in Gelato v4. |

### Shipment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Shipment Methods](actions/shipment-methods.md) | GET | Finds Gelato shipment methods by destination country. |

### Stock Availability

| Action | Method | Description |
| --- | --- | --- |
| [Stock Availability](actions/stock-availability.md) | GET | Retrieves regional stock availability for Gelato products. |

