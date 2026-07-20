# WEBLUCY: Native API Reference

A consolidated summary of WEBLUCY's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://websitebuilder.docs.apiary.io
- **API base URL:** `https://apps.weblucy.com/api/site`

## Authentication

### API Key

Use the API key from Website Settings > Applications > API Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://websitebuilder.docs.apiary.io/#reference/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `MindCloud/1.0` |

## Pagination

Use `limit` in the query string to set the page size (default 30; accepted range 1–50). Use `skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://websitebuilder.docs.apiary.io/#reference/contacts/list-and-create/create-new-contact) |
| [Create Member](actions/create-member.md) | `POST /members` | [docs](https://websitebuilder.docs.apiary.io/#reference/members/list-and-create/create-new-member) |
| [Create Member Group](actions/create-member-group.md) | `POST /member-groups` | [docs](https://websitebuilder.docs.apiary.io/#reference/member-groups/list-and-create/create-new-member-group) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://websitebuilder.docs.apiary.io/#reference/products/list-and-create/create-new-product) |
| [Create Subscriber List](actions/create-subscriber-list.md) | `POST /subscriber-lists` | [docs](https://websitebuilder.docs.apiary.io/#reference/subscriber-lists/list-and-create/create-new-subscriber-list) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://websitebuilder.docs.apiary.io/#reference/webhooks/list-and-create/create-new-webhook) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/contacts/single-contact/delete-contact) |
| [Delete Member](actions/delete-member.md) | `DELETE /members/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/members/single-member/delete-member) |
| [Delete Member Group](actions/delete-member-group.md) | `DELETE /member-groups/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/member-groups/single-member-group/delete-member-group) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/products/single-product/delete-product) |
| [Delete Subscriber List](actions/delete-subscriber-list.md) | `DELETE /subscriber-lists/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/subscriber-lists/single-list/delete-subscriber-list) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/webhooks/single-webhook/delete-webhook) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/contacts/single-contact/retrieve-contact) |
| [Get Member](actions/get-member.md) | `GET /members/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/members/single-member/retrieve-member) |
| [Get Member Group](actions/get-member-group.md) | `GET /member-groups/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/member-groups/single-member-group/retrieve-member-group) |
| [Get Order](actions/get-order.md) | `GET /orders/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/orders/single-order/retrieve-order) |
| [Get Product](actions/get-product.md) | `GET /products/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/products/single-product/retrieve-product) |
| [Get Subscriber List](actions/get-subscriber-list.md) | `GET /subscriber-lists/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/subscriber-lists/single-list/retrieve-subscriber-list) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://websitebuilder.docs.apiary.io/#reference/bookings/list-all-bookings/list-all-bookings) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://websitebuilder.docs.apiary.io/#reference/contacts/list-and-create/list-all-contacts) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /form-submissions` | [docs](https://websitebuilder.docs.apiary.io/#reference/form-submissions/list-all-form-submissions/list-all-form-submissions) |
| [List Member Groups](actions/list-member-groups.md) | `GET /member-groups` | [docs](https://websitebuilder.docs.apiary.io/#reference/member-groups/list-and-create/list-all-member-groups) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://websitebuilder.docs.apiary.io/#reference/members/list-and-create/list-all-members) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://websitebuilder.docs.apiary.io/#reference/orders/list/list-all-orders) |
| [List Product Categories](actions/list-product-categories.md) | `GET /products/categories` | [docs](https://websitebuilder.docs.apiary.io/#reference/products/categories/list-all-categories) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://websitebuilder.docs.apiary.io/#reference/products/list-and-create/list-all-products) |
| [List Subscriber Lists](actions/list-subscriber-lists.md) | `GET /subscriber-lists` | [docs](https://websitebuilder.docs.apiary.io/#reference/subscriber-lists/list-and-create/list-all-subscriber-lists) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://websitebuilder.docs.apiary.io/#reference/webhooks/list-and-create/list-all-webhooks) |
| [Search Contact by Email](actions/search-contact-by-email.md) | `GET /contacts/search-by-email` | [docs](https://websitebuilder.docs.apiary.io/#reference/contacts/search-contacts/search-by-email) |
| [Search Member by Email](actions/search-member-by-email.md) | `GET /members/search-by-email` | [docs](https://websitebuilder.docs.apiary.io/#reference/members/search-members/search-by-email) |
| [Start Member Session](actions/start-member-session.md) | `POST /members/start-session` | [docs](https://websitebuilder.docs.apiary.io/#reference/members/single-sign-on/start-member-session) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/contacts/single-contact/update-contact) |
| [Update Member](actions/update-member.md) | `PUT /members/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/members/single-member/update-member) |
| [Update Member Group](actions/update-member-group.md) | `PUT /member-groups/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/member-groups/single-member-group/update-member-group) |
| [Update Order](actions/update-order.md) | `PUT /orders/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/orders/single-order/update-order) |
| [Update Product](actions/update-product.md) | `PUT /products/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/products/single-product/update-product) |
| [Update Subscriber List](actions/update-subscriber-list.md) | `PUT /subscriber-lists/{id}` | [docs](https://websitebuilder.docs.apiary.io/#reference/subscriber-lists/single-list/update-subscriber-list) |
