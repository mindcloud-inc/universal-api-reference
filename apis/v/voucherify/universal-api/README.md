# <img src="https://images.mindcloud.co/apps/icons/voucherify-apple-touch-icon_1775838134660.png" alt="Voucherify logo" width="28" height="28"> Voucherify: Universal API

Voucherify helps teams create, validate, publish, and redeem vouchers, promotions, and loyalty campaigns through the Voucherify REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/voucherify/latest
- **Actions:** 51
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.voucherify.io
- **Vendor API docs:** https://docs.voucherify.io/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (51)

### Async Action

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Action](actions/get-async-action.md) | GET | Retrieves an async action from Voucherify. |
| [List Async Actions](actions/list-async-actions.md) | GET | Retrieves a list of async actions from Voucherify. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Voucherify. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves a list of campaigns from Voucherify. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Voucherify. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes an existing category from Voucherify. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Voucherify. |
| [List Categories](actions/list-categories.md) | GET | Retrieves a list of categories from Voucherify. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in Voucherify. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Voucherify, or updates an existing one. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Voucherify. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Voucherify. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from Voucherify. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Voucherify. |

### Export

| Action | Method | Description |
| --- | --- | --- |
| [Create Export](actions/create-export.md) | POST | Creates a new export in Voucherify. |
| [Get Export](actions/get-export.md) | GET | Retrieves an export from Voucherify. |
| [List Exports](actions/list-exports.md) | GET | Retrieves a list of exports from Voucherify. |

### Loyalty Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Loyalty Campaigns](actions/list-loyalty-campaigns.md) | GET | Retrieves a list of loyalty campaigns from Voucherify. |

### Metadata Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Metadata Schema](actions/get-metadata-schema.md) | GET | Retrieves a metadata schema from Voucherify. |
| [List Metadata Schemas](actions/list-metadata-schemas.md) | GET | Retrieves a list of metadata schemas from Voucherify. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Voucherify. |
| [List Orders](actions/list-orders.md) | GET | Retrieves a list of orders from Voucherify. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Voucherify, or updates an existing one. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Voucherify. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Voucherify. |
| [List Products](actions/list-products.md) | GET | Retrieves a list of products from Voucherify. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Voucherify. |

### Product Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Collection](actions/get-product-collection.md) | GET | Retrieves a product collection from Voucherify. |
| [List Product Collections](actions/list-product-collections.md) | GET | Retrieves a list of product collections from Voucherify. |

### Publication

| Action | Method | Description |
| --- | --- | --- |
| [Create Publication](actions/create-publication.md) | POST | Creates a publication in Voucherify for eligible vouchers. |
| [Get Publication](actions/get-publication.md) | GET |  |
| [List Publications](actions/list-publications.md) | GET | Retrieves a list of publications from Voucherify. |
| [List Voucher Publications](actions/list-voucher-publications.md) | GET | Retrieves a voucher's publications from Voucherify. |

### Redemption

| Action | Method | Description |
| --- | --- | --- |
| [Create Redemption](actions/create-redemption.md) | POST | Creates a redemption in Voucherify. |
| [Get Redemption](actions/get-redemption.md) | GET | Retrieves a redemption from Voucherify. |
| [List Redemptions](actions/list-redemptions.md) | GET | Retrieves a list of redemptions from Voucherify. |
| [List Voucher Redemptions](actions/list-voucher-redemptions.md) | GET | Retrieves a voucher's redemptions from Voucherify. |

### Reward

| Action | Method | Description |
| --- | --- | --- |
| [Get Reward](actions/get-reward.md) | GET | Retrieves a reward from Voucherify. |
| [List Rewards](actions/list-rewards.md) | GET | Retrieves a list of rewards from Voucherify. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from Voucherify. |
| [List Segments](actions/list-segments.md) | GET | Retrieves a list of segments from Voucherify. |

### Validation Rule

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation Rule](actions/get-validation-rule.md) | GET | Retrieves a validation rule from Voucherify. |
| [List Validation Rules](actions/list-validation-rules.md) | GET | Retrieves a list of validation rules from Voucherify. |

### Validation Rule Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Get Validation Rule Assignment](actions/get-validation-rule-assignment.md) | GET |  |
| [List Validation Rule Assignments](actions/list-validation-rule-assignments.md) | GET | Retrieves validation rule assignments from Voucherify. |

### Voucher

| Action | Method | Description |
| --- | --- | --- |
| [Create Voucher](actions/create-voucher.md) | POST | Creates a new voucher in Voucherify. |
| [Delete Voucher](actions/delete-voucher.md) | DELETE | Deletes an existing voucher from Voucherify. |
| [Get Voucher](actions/get-voucher.md) | GET | Retrieves a voucher from Voucherify by code or ID. |
| [List Vouchers](actions/list-vouchers.md) | GET | Retrieves a list of vouchers from Voucherify. |
| [Update Voucher](actions/update-voucher.md) | PUT | Updates an existing voucher in Voucherify. |

### Voucher Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List Voucher Transactions](actions/list-voucher-transactions.md) | GET | Retrieves a voucher's transactions from Voucherify. |

