# <img src="https://images.mindcloud.co/apps/icons/sellty_1776867196487.png" alt="Sellty logo" width="28" height="28"> Sellty: Universal API

Manage Sellty products, orders, categories, and groups

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sellty/latest
- **Category:** Commerce
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sellty.ru
- **Vendor API docs:** https://my.sellty.ru/seller/api/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Categories](actions/list-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sellty/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET |  |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET |  |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |
| [List Orders By Email](actions/list-orders-by-email.md) | GET |  |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Delete Product](actions/delete-product.md) | DELETE |  |
| [List Products](actions/list-products.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

