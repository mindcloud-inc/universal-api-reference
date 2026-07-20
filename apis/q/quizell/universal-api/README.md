# <img src="https://images.mindcloud.co/apps/icons/quizell_1774871454608.png" alt="Quizell logo" width="28" height="28"> Quizell: Universal API

Build quizzes, manage products, and capture customer responses

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quizell/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quizell.com
- **Vendor API docs:** https://docs.quizell.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Products](actions/search-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quizell/latest/actions/search-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Custom Field](actions/create-customer-custom-field.md) | POST | Creates a customer custom field in Quizell. |
| [Delete Customer Custom Field](actions/delete-customer-custom-field.md) | DELETE | Deletes a customer custom field from Quizell. |
| [List Customer Custom Fields](actions/list-customer-custom-fields.md) | GET | Retrieves customer custom fields from Quizell. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Quizell. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Quizell. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Quizell by ID. |
| [List Customers](actions/list-customers.md) | GET | Finds customers in Quizell with search and pagination. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Quizell. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Batch Products](actions/batch-products.md) | POST | Creates multiple products in Quizell. |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Quizell. |
| [Delete Multiple Products](actions/delete-multiple-products.md) | DELETE | Deletes multiple products from Quizell. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Quizell. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Quizell by ID. |
| [Search Products](actions/search-products.md) | GET | Finds products in Quizell by title or SKU. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Quizell. |

