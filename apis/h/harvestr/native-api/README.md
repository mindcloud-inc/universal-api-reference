# Harvestr.io: Native API Reference

A consolidated summary of Harvestr.io's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developers.harvestr.io/api/
- **API base URL:** `https://rest.harvestr.io/v1`

## Authentication

### API Key

Create a Harvestr private app token and send it in the X-Harvestr-Private-App-Token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.harvestr.io/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /company` | [docs](https://developers.harvestr.io/api/create-a-company/) |
| [Create Feedback](actions/create-feedback.md) | `POST /feedback` | [docs](https://developers.harvestr.io/api/create-a-feedback-link-a-message-to-a-discovery/) |
| [Create Message](actions/create-message.md) | `POST /message` | [docs](https://developers.harvestr.io/api/create-a-message/) |
| [Create User](actions/create-user.md) | `POST /user` | [docs](https://developers.harvestr.io/api/create-a-user/) |
| [Get Discovery State](actions/get-discovery-state.md) | `GET /discovery/{id}/discovery-state` | [docs](https://developers.harvestr.io/api/get-discoverys-discovery-state/) |
| [List Companies](actions/list-companies.md) | `GET /company` | [docs](https://developers.harvestr.io/api/list-companies/) |
| [List Company Attribute Values](actions/list-company-attribute-values.md) | `GET /company/{id}/attribute-value` | [docs](https://developers.harvestr.io/api/list-companys-attribute-values/) |
| [List Company Attributes](actions/list-company-attributes.md) | `GET /attribute/company` | [docs](https://developers.harvestr.io/api/list-companies-attributes/) |
| [List Components](actions/list-components.md) | `GET /component` | [docs](https://developers.harvestr.io/api/list-components/) |
| [List Custom Inboxes](actions/list-custom-inboxes.md) | `GET /custom-inbox` | [docs](https://developers.harvestr.io/api/list-custom-inboxes/) |
| [List Discoveries](actions/list-discoveries.md) | `GET /discovery` | [docs](https://developers.harvestr.io/api/list-discoveries/) |
| [List Discovery Feedback](actions/list-discovery-feedback.md) | `GET /discovery/{id}/feedback` | [docs](https://developers.harvestr.io/api/list-discoveriess-feedback/) |
| [List Discovery States](actions/list-discovery-states.md) | `GET /discovery-state` | [docs](https://developers.harvestr.io/api/list-discovery-states/) |
| [List Feedback](actions/list-feedback.md) | `GET /feedback` | [docs](https://developers.harvestr.io/api/list-feedback/) |
| [List Message Feedback](actions/list-message-feedback.md) | `GET /message/{id}/feedback` | [docs](https://developers.harvestr.io/api/list-messages-feedback/) |
| [List Messages](actions/list-messages.md) | `GET /message` | [docs](https://developers.harvestr.io/api/list-messages/) |
| [List User Attribute Values](actions/list-user-attribute-values.md) | `GET /user/{id}/attribute-value` | [docs](https://developers.harvestr.io/api/list-users-attribute-values/) |
| [List User Attributes](actions/list-user-attributes.md) | `GET /attribute/user` | [docs](https://developers.harvestr.io/api/list-users-attributes/) |
| [List Users](actions/list-users.md) | `GET /user` | [docs](https://developers.harvestr.io/api/list-users/) |
| [Retrieve Company](actions/retrieve-company.md) | `GET /company/{id}` | [docs](https://developers.harvestr.io/api/retrieve-a-company/) |
| [Retrieve Component](actions/retrieve-component.md) | `GET /component/{id}` | [docs](https://developers.harvestr.io/api/retrieve-a-component/) |
| [Retrieve Discovery](actions/retrieve-discovery.md) | `GET /discovery/{id}` | [docs](https://developers.harvestr.io/api/retrieve-a-discovery/) |
| [Retrieve Discovery State](actions/retrieve-discovery-state.md) | `GET /discovery-state/{id}` | [docs](https://developers.harvestr.io/api/retrieve-discovery-state/) |
| [Retrieve Feedback](actions/retrieve-feedback.md) | `GET /feedback/{id}` | [docs](https://developers.harvestr.io/api/retrieve-a-feedback/) |
| [Retrieve Message](actions/retrieve-message.md) | `GET /message/{id}` | [docs](https://developers.harvestr.io/api/retrieve-a-message/) |
| [Retrieve User](actions/retrieve-user.md) | `GET /user/{id}` | [docs](https://developers.harvestr.io/api/retrieve-a-user/) |
| [Update Company](actions/update-company.md) | `PATCH /company/{id}` | [docs](https://developers.harvestr.io/api/update-a-company/) |
| [Update Company Attribute Values](actions/update-company-attribute-values.md) | `PATCH /company/{id}/attribute/{attributeId}` | [docs](https://developers.harvestr.io/api/update-attribute-values-from-a-company/) |
| [Update Discovery](actions/update-discovery.md) | `PATCH /discovery/{id}` | [docs](https://developers.harvestr.io/api/update-a-discovery/) |
| [Update Message](actions/update-message.md) | `PATCH /message/{id}` | [docs](https://developers.harvestr.io/api/update-a-message/) |
| [Update User](actions/update-user.md) | `PATCH /user/{id}` | [docs](https://developers.harvestr.io/api/update-a-user/) |
| [Update User Attribute Values](actions/update-user-attribute-values.md) | `PATCH /user/{id}/attribute/{attributeId}` | [docs](https://developers.harvestr.io/api/update-attribute-values-from-a-user/) |
