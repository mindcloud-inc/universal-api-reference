# ForceManager: Native API Reference

A consolidated summary of ForceManager's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://support.forcemanager.net/en/articles/8613479-using-restful-api

## Authentication

### Signed API Keys

ForceManager requires a support-issued public API key and private API key. Requests are authenticated with X-FM-PublicKey, X-FM-UnixTimestamp, and X-FM-Signature headers, where the signature is sha1(UnixTimestamp + APIPublicKey + APIPrivateKey).

### Credentials

- **Public API Key:** `publicKey` · required · Public API key issued by ForceManager support.
- **Private API Key:** `privateKey` · required · Private API key issued by ForceManager support. This is used to compute the X-FM-Signature header and must never be sent in plain text.

[Official authentication documentation](https://support.forcemanager.net/en/articles/8613476-authentication-in-sage-sales-management-api)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /activities` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Create Calendar](actions/create-calendar.md) | `POST /calendars` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /opportunities` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Create View](actions/create-view.md) | `POST /views` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Delete Activity](actions/delete-activity.md) | `DELETE /activities` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Delete Calendar](actions/delete-calendar.md) | `DELETE /calendars` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Delete Company](actions/delete-company.md) | `DELETE /companies` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Delete Opportunity](actions/delete-opportunity.md) | `DELETE /opportunities` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Delete Product](actions/delete-product.md) | `DELETE /products` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Delete View](actions/delete-view.md) | `DELETE /views` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Read Activities](actions/read-activities.md) | `GET /activities` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Read Calendars](actions/read-calendars.md) | `GET /calendars` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Read Companies](actions/read-companies.md) | `GET /companies` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Read Contacts](actions/read-contacts.md) | `GET /contacts` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Read Opportunities](actions/read-opportunities.md) | `GET /opportunities` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Read Products](actions/read-products.md) | `GET /products` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Read Sales Orders](actions/read-sales-orders.md) | `GET /salesorder` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Read Users](actions/read-users.md) | `GET /users` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Read Views](actions/read-views.md) | `GET /views` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Update Activity](actions/update-activity.md) | `PUT /activities` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Update Calendar](actions/update-calendar.md) | `PUT /calendars` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Update Company](actions/update-company.md) | `PUT /companies` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Update Opportunity](actions/update-opportunity.md) | `PUT /opportunities` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Update Product](actions/update-product.md) | `PUT /products` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
| [Update View](actions/update-view.md) | `PUT /views` | [docs](https://support.forcemanager.net/en/articles/8613478-entity-types) |
