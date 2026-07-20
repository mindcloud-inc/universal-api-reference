# <img src="https://images.mindcloud.co/apps/icons/weblucy-icon-square_1776105937272.png" alt="WEBLUCY logo" width="28" height="28"> WEBLUCY: Universal API

WEBLUCY is a website builder and CRM platform with REST APIs for contacts, members, products, orders, forms, bookings, subscriber lists, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wEBLUCY/latest
- **Category:** Website & App Building / CMS
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://weblucy.com
- **Vendor API docs:** https://websitebuilder.docs.apiary.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contacts](actions/list-contacts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from WEBLUCY. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Product Categories](actions/list-product-categories.md) | GET | Retrieves product categories from WEBLUCY. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in WEBLUCY. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from WEBLUCY. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from WEBLUCY. |
| [Search Contact by Email](actions/search-contact-by-email.md) | GET | Finds contacts in WEBLUCY by email address. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in WEBLUCY. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from WEBLUCY. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Retrieves form submissions from WEBLUCY. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Member Group](actions/create-member-group.md) | POST | Creates a new member group in WEBLUCY. |
| [Delete Member Group](actions/delete-member-group.md) | DELETE | Deletes an existing member group from WEBLUCY. |
| [Get Member Group](actions/get-member-group.md) | GET | Retrieves a member group from WEBLUCY. |
| [List Member Groups](actions/list-member-groups.md) | GET | Retrieves member groups from WEBLUCY. |
| [Update Member Group](actions/update-member-group.md) | PUT | Updates an existing member group in WEBLUCY. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber List](actions/create-subscriber-list.md) | POST | Creates a new subscriber list in WEBLUCY. |
| [Delete Subscriber List](actions/delete-subscriber-list.md) | DELETE | Deletes an existing subscriber list from WEBLUCY. |
| [Get Subscriber List](actions/get-subscriber-list.md) | GET | Retrieves a subscriber list from WEBLUCY. |
| [List Subscriber Lists](actions/list-subscriber-lists.md) | GET | Retrieves subscriber lists from WEBLUCY. |
| [Update Subscriber List](actions/update-subscriber-list.md) | PUT | Updates an existing subscriber list in WEBLUCY. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST | Creates a new member in WEBLUCY. |
| [Delete Member](actions/delete-member.md) | DELETE | Deletes an existing member from WEBLUCY. |
| [Get Member](actions/get-member.md) | GET | Retrieves a member from WEBLUCY. |
| [List Members](actions/list-members.md) | GET | Retrieves members from WEBLUCY. |
| [Search Member by Email](actions/search-member-by-email.md) | GET | Finds members in WEBLUCY by email address. |
| [Update Member](actions/update-member.md) | PUT | Updates an existing member in WEBLUCY. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from WEBLUCY. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from WEBLUCY. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in WEBLUCY. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in WEBLUCY. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from WEBLUCY. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from WEBLUCY. |
| [List Products](actions/list-products.md) | GET | Retrieves products from WEBLUCY. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in WEBLUCY. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Start Member Session](actions/start-member-session.md) | POST | Starts a member session in WEBLUCY. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in WEBLUCY. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from WEBLUCY. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from WEBLUCY. |

