# <img src="https://images.mindcloud.co/apps/icons/g2_1782742991833.png" alt="G2 logo" width="28" height="28"> G2: Universal API

Access buyer intent, reviews, products, and categories from G2

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/g2/latest
- **Category:** Marketing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.g2.com
- **Vendor API docs:** https://data.g2.com/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Categories](actions/list-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/g2/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from G2. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from G2. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from G2. |
| [List Products](actions/list-products.md) | GET | Retrieves products from G2. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Browse Product Buyer Intent](actions/browse-product-buyer-intent.md) | GET | Retrieves buyer intent interactions for a product in G2. |
| [Retrieve Market Signals](actions/retrieve-market-signals.md) | GET | Retrieves category buyer intent signals from G2 for a date range. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Question](actions/get-question.md) | GET | Retrieves a question from G2. |
| [List Questions](actions/list-questions.md) | GET | Retrieves questions from G2. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendor](actions/get-vendor.md) | GET | Retrieves a vendor from G2. |
| [List Vendors](actions/list-vendors.md) | GET | Retrieves vendors from G2. |

