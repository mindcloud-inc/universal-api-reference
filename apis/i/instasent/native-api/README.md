# Instasent: Native API Reference

A consolidated summary of Instasent's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api
- **API base URL:** `https://api.instasent.com/v1`

## Authentication

### Project Token

Use an Instasent project token with access to the projects and permissions needed for Product API reads and sends.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.instasent.com/en/articles/9071958-api-tokens)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Aggregate Audience](actions/aggregate-audience.md) | `POST /project/:project/audience/aggregations` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Create Datasource](actions/create-datasource.md) | `POST /project/:project/datasource` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Delete Stream Record](actions/delete-stream-record.md) | `DELETE /project/:project/datasource/:datasource/stream/:action/:userId` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Audience Contact](actions/get-audience-contact.md) | `GET /project/:project/audience/:audienceId` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Audience Contact by User ID](actions/get-audience-contact-by-user-id.md) | `GET /project/:project/audience/user/:userId` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Datasource](actions/get-datasource.md) | `GET /project/:project/datasource/:id` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Datasource Stats](actions/get-datasource-stats.md) | `GET /project/:project/datasource/:datasource/stats` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Datasource Stream](actions/get-datasource-stream.md) | `GET /project/:project/datasource/:datasource/stream` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Datasource Stream Specs](actions/get-datasource-stream-specs.md) | `GET /project/:project/datasource/:datasource/stream/specs/:spec` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Event Parameter Specs](actions/get-event-parameter-specs.md) | `GET /project/:project/specs/events/:eventType` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Project Attribute Specs](actions/get-project-attribute-specs.md) | `GET /project/:project/specs/attributes` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Project Event Specs](actions/get-project-event-specs.md) | `GET /project/:project/specs/events` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Project Info](actions/get-project-info.md) | `GET /project/:project` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get SMS](actions/get-sms.md) | `GET /project/:project/channel/sms/sms/:id` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Get Stream Contact](actions/get-stream-contact.md) | `GET /project/:project/datasource/:datasource/stream/contacts/:userId` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [List Datasources](actions/list-datasources.md) | `GET /project/:project/datasource` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [List Projects](actions/list-projects.md) | `GET /` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [List SMS Senders](actions/list-sms-senders.md) | `GET /project/:project/channel/sms/sender` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Push Stream Data](actions/push-stream-data.md) | `POST /project/:project/datasource/:datasource/stream/:action` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Scroll Audience](actions/scroll-audience.md) | `POST /project/:project/audience/scroll` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Search Audience](actions/search-audience.md) | `POST /project/:project/audience/search` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Search Audience by Email](actions/search-audience-by-email.md) | `GET /project/:project/audience/search/email/:userEmail` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Search Audience by Phone](actions/search-audience-by-phone.md) | `GET /project/:project/audience/search/phone/:userPhone` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
| [Send Direct SMS](actions/send-direct-sms.md) | `POST /project/:project/channel/sms/sms/direct/:senderId/:audienceId` | [docs](https://instasent.stoplight.io/docs/instasent/8j57yi7wown1z-instasent-product-api) |
