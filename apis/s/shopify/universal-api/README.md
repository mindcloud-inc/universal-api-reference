# <img src="https://images.mindcloud.co/apps/icons/shopify_1776706561167.png" alt="Shopify logo" width="28" height="28"> Shopify: Universal API

Manage products, orders, customers, and inventory levels

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shopify/latest
- **Category:** Commerce
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** shopify.com
- **Vendor API docs:** https://shopify.dev/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Admin Graphql Api

| Action | Method | Description |
| --- | --- | --- |
| [GraphQL - Get Records (Paginated)](actions/graphql-get-records-paginated.md) | GET | Retrieves records from Shopify with paginated GraphQL queries. |
| [GraphQL - Get Records (Unwrapped Edges)](actions/graphql-get-records-unwrapped-edges.md) | GET | Retrieves records from Shopify from nested GraphQL edges. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [List Publication Channels](actions/list-publication-channels.md) | GET | Retrieves publication channels from Shopify. |
| [List Selling Plan Groups](actions/list-selling-plan-groups.md) | GET | Retrieves selling plan groups from Shopify. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies-graphql.md) | GET | Retrieves companies from Shopify with GraphQL. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Deleted Product Events](actions/list-deleted-product-events.md) | GET | Retrieves deleted product events from Shopify. |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [Start Inventory Bulk Export](actions/start-inventory-bulk-export.md) | GET |  |

### Inventory Export

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Bulk Export Status](actions/get-inventory-bulk-export-status.md) | GET |  |

### Inventory Levels

| Action | Method | Description |
| --- | --- | --- |
| [Activate Inventory Item](actions/activate-inventory-item.md) | POST | Activates an inventory item in Shopify. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from Shopify. |

### Order Payment Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Order Payment Transactions](actions/get-order-transactions-graph-ql.md) | GET |  |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Variant by SKU](actions/get-product-variant-by-sku.md) | GET | Finds product variants in Shopify by SKU. |
| [List Product Variants](actions/list-product-variants.md) | GET | Retrieves product variants from Shopify. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from Shopify with GraphQL. |
| [Update Product (GraphQL)](actions/update-product-graphql.md) | PUT | Updates an existing product in Shopify. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers-graphql.md) | GET | Retrieves customers from Shopify with GraphQL. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [List All Orders](actions/list-all-orders-graphql.md) | GET | Retrieves orders from Shopify with GraphQL. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Shopify with GraphQL. |

### Webhooks

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription (HTTP)](actions/create-webhook-subscription-http.md) | POST | Creates an HTTP webhook subscription in Shopify. |

