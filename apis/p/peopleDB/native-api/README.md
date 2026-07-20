# PeopleDB: Native API Reference

A consolidated summary of PeopleDB's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docs.peopledb.co
- **OpenAPI specification:** https://docs.peopledb.co/openapi.yaml
- **API base URL:** `https://peopledb.co/api/v1`

## Authentication

### API Key

Use your PeopleDB API key. The runtime sends it as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.peopledb.co/openapi.yaml)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Contact Info by GitHub ID](actions/get-contact-info-by-git-hub-id.md) | `GET /people` | [docs](https://docs.peopledb.co/openapi.yaml) |
| [Get Contact Info by GitHub Username](actions/get-contact-info-by-git-hub-username.md) | `GET /people` | [docs](https://docs.peopledb.co/openapi.yaml) |
| [Get Contact Info by LinkedIn ID](actions/get-contact-info-by-linked-in-id.md) | `GET /people` | [docs](https://docs.peopledb.co/openapi.yaml) |
| [Get Contact Info by LinkedIn Username](actions/get-contact-info-by-linked-in-username.md) | `GET /people` | [docs](https://docs.peopledb.co/openapi.yaml) |
| [Validate Email Address](actions/validate-email-address.md) | `GET /email_verifications` | [docs](https://docs.peopledb.co/openapi.yaml) |
| [Validate Email Address via POST](actions/validate-email-address-post.md) | `POST /email_verifications` | [docs](https://docs.peopledb.co/openapi.yaml) |
