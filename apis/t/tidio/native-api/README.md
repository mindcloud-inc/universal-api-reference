# Tidio: Native API Reference

A consolidated summary of Tidio's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://developers.tidio.com/reference
- **API base URL:** `https://api.tidio.com`

## Authentication

### OpenAPI Keys

Authenticate with Tidio OpenAPI client ID and client secret headers.

### Credentials

- **Client ID:** `clientId` · required · Paste the Tidio OpenAPI Client ID (ci_...).
- **Client Secret:** `clientSecret` · required · Paste the Tidio OpenAPI Client Secret (cs_...).

[Official authentication documentation](https://developers.tidio.com/docs/openapi-authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json; version=1` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `cursor` in the query string as the pagination cursor.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Website as Lyro Data Source [Plus plan]](actions/add-website-as-lyro-data-source-plus-plan.md) | `POST /lyro/data-sources/website/scrape` | [docs](https://developers.tidio.com/reference/post_lyro-data-sources-website-scrape) |
| [Ask Lyro [Plus plan]](actions/ask-lyro-plus-plan.md) | `POST /lyro/tickets` | [docs](https://developers.tidio.com/reference/post_lyro-tickets) |
| [Create Contact [Plus plan]](actions/create-contact-plus-plan.md) | `POST /contacts` | [docs](https://developers.tidio.com/reference/post_contacts) |
| [Create Lyro QA Data Source [Plus plan]](actions/create-lyro-qa-data-source-plus-plan.md) | `POST /lyro/data-sources/qa` | [docs](https://developers.tidio.com/reference/post_lyro-data-sources-qa) |
| [Create Multiple Contacts [Plus plan]](actions/create-multiple-contacts-plus-plan.md) | `POST /contacts/batch` | [docs](https://developers.tidio.com/reference/post_contacts-batch) |
| [Create Ticket (As Contact) [Plus plan]](actions/create-ticket-as-contact-plus-plan.md) | `POST /tickets/as-contact` | [docs](https://developers.tidio.com/reference/post_tickets-as-contact) |
| [Delete Contact [Plus plan]](actions/delete-contact-plus-plan.md) | `DELETE /contacts/{contactId}` | [docs](https://developers.tidio.com/reference/delete_contacts-contactid) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/{productId}` | [docs](https://developers.tidio.com/reference/delete_products-productid) |
| [Delete Ticket [Plus plan]](actions/delete-ticket-plus-plan.md) | `DELETE /tickets/{ticketId}` | [docs](https://developers.tidio.com/reference/delete_tickets-ticketid) |
| [Get Contact Messages [Plus plan]](actions/get-contact-messages-plus-plan.md) | `GET /contacts/{contactId}/messages` | [docs](https://developers.tidio.com/reference/get_contacts-contactid-messages) |
| [Get Contact [Plus plan]](actions/get-contact-plus-plan.md) | `GET /contacts/{contactId}` | [docs](https://developers.tidio.com/reference/get_contacts-contactid) |
| [Get Project Info [Plus plan]](actions/get-project-info-plus-plan.md) | `GET /project` | [docs](https://developers.tidio.com/reference/get_project) |
| [Get Ticket Details [Plus plan]](actions/get-ticket-details-plus-plan.md) | `GET /tickets/{ticketId}` | [docs](https://developers.tidio.com/reference/get_tickets-ticketid) |
| [Get Viewed Pages History [Plus plan]](actions/get-viewed-pages-history-plus-plan.md) | `GET /contacts/{contactId}/viewed-pages` | [docs](https://developers.tidio.com/reference/get_contacts-contactid-viewed-pages) |
| [List Contact Properties [Plus plan]](actions/list-contact-properties-plus-plan.md) | `GET /contact-properties` | [docs](https://developers.tidio.com/reference/get_contact-properties) |
| [List Contacts [Plus plan]](actions/list-contacts-plus-plan.md) | `GET /contacts` | [docs](https://developers.tidio.com/reference/get_contacts) |
| [List Departments [Plus plan]](actions/list-departments-plus-plan.md) | `GET /departments` | [docs](https://developers.tidio.com/reference/get_departments) |
| [List Operators [Plus plan]](actions/list-operators-plus-plan.md) | `GET /operators` | [docs](https://developers.tidio.com/reference/get_operators) |
| [List Tickets [Plus plan]](actions/list-tickets-plus-plan.md) | `GET /tickets` | [docs](https://developers.tidio.com/reference/get_tickets) |
| [Reply to Ticket [Plus plan]](actions/reply-to-ticket-plus-plan.md) | `POST /tickets/{ticketId}/reply` | [docs](https://developers.tidio.com/reference/post_tickets-ticketid-reply) |
| [Update Contact Properties [Plus plan]](actions/update-contact-properties-plus-plan.md) | `PATCH /contacts/{contactId}` | [docs](https://developers.tidio.com/reference/patch_contacts-contactid) |
| [Update Multiple Contacts [Plus plan]](actions/update-multiple-contacts-plus-plan.md) | `PATCH /contacts/batch` | [docs](https://developers.tidio.com/reference/patch_contacts-batch) |
| [Update Ticket [Plus plan]](actions/update-ticket-plus-plan.md) | `PATCH /tickets/{ticketId}` | [docs](https://developers.tidio.com/reference/patch_tickets-ticketid) |
| [Upsert Lyro Data Source [Plus plan]](actions/upsert-lyro-data-source-plus-plan.md) | `PUT /lyro/data-sources/website` | [docs](https://developers.tidio.com/reference/put_lyro-data-sources-website) |
| [Upsert Products](actions/upsert-products.md) | `PUT /products/batch` | [docs](https://developers.tidio.com/reference/put_products-batch) |
