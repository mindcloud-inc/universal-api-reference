# <img src="https://images.mindcloud.co/apps/icons/images-11_1775827318930.png" alt="Open Letter Connect logo" width="28" height="28"> Open Letter Connect: Universal API

Manage direct mail operations in Open Letter Connect, including products, templates, contacts, custom fields, order proofs, and order history.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openLetterConnect/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://openletterconnect.com/
- **Vendor API docs:** https://api-docs.openletterconnect.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Product Types](actions/get-product-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/get-product-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a contact in Open Letter Connect. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes a contact from Open Letter Connect. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Open Letter Connect. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Open Letter Connect. |
| [Update Contact](actions/update-contact.md) | PUT | Updates a contact in Open Letter Connect. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | POST | Creates a custom field in Open Letter Connect. |
| [Delete Custom Field](actions/delete-custom-field.md) | DELETE | Deletes a custom field from Open Letter Connect. |
| [Get Custom Field](actions/get-custom-field.md) | GET | Retrieves a custom field from Open Letter Connect. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from Open Letter Connect. |
| [Update Custom Field](actions/update-custom-field.md) | PUT | Updates a custom field in Open Letter Connect. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates an order in Open Letter Connect. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Open Letter Connect. |
| [Get Order Details](actions/get-order-details.md) | GET | Retrieves order details from Open Letter Connect. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Open Letter Connect. |
| [View Order Proof](actions/view-order-proof.md) | GET | Retrieves an order proof from Open Letter Connect. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Details](actions/get-product-details.md) | GET | Retrieves product details from Open Letter Connect. |
| [Get Product Types](actions/get-product-types.md) | GET | Retrieves product types from Open Letter Connect. |
| [List Products](actions/list-products.md) | GET | Retrieves products from Open Letter Connect. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a template in Open Letter Connect. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes a template from Open Letter Connect. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Open Letter Connect. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Open Letter Connect. |
| [Update Template](actions/update-template.md) | PUT | Updates a template in Open Letter Connect. |
| [Upload Template](actions/upload-template.md) | POST | Uploads a template to Open Letter Connect. |

