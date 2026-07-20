# <img src="https://images.mindcloud.co/apps/icons/favicon-23_1776271207012.png" alt="MailBluster logo" width="28" height="28"> MailBluster: Universal API

Manage MailBluster email marketing resources including leads, custom fields, products, orders, and ecommerce activity through the MailBluster API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailBluster/latest
- **Category:** Communication / Email Communications
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mailbluster.com
- **Vendor API docs:** https://app.mailbluster.com/api-doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Fields](actions/list-fields.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET | Retrieves all custom fields from MailBluster. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in MailBluster. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from MailBluster by lead hash. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from MailBluster by lead hash. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in MailBluster by lead hash. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in MailBluster. |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an existing order from MailBluster. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from MailBluster. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a page of orders from MailBluster. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in MailBluster. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in MailBluster. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from MailBluster. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from MailBluster. |
| [List Products](actions/list-products.md) | GET | Retrieves a page of products from MailBluster. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in MailBluster. |

