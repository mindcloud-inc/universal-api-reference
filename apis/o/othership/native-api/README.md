# Othership: Native API Reference

A consolidated summary of Othership's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://knowledge.othership.com/workplace-software-faq-admins?hsLang=en
- **API base URL:** `https://hwms-api.othership.com/api/v1/azure/scim`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://knowledge.othership.com/scim-provisioning-with-microsoft-entra-id-for-othership-workplace-scheduler)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/scim+json` |
| `Content-Type` | `application/scim+json` |

Responses from this API use JSON. Response data is read from `Resources`.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | `POST /Groups` | [docs](https://www.ietf.org/rfc/rfc7644) |
| [Create User](actions/create-user.md) | `POST /Users` | [docs](https://www.ietf.org/rfc/rfc7644) |
| [Deactivate User](actions/deactivate-user.md) | `PATCH /Users/:id` | [docs](https://www.ietf.org/rfc/rfc7644) |
| [Get Group](actions/get-group.md) | `GET /Groups/:id` | [docs](https://www.ietf.org/rfc/rfc7644) |
| [Get User](actions/get-user.md) | `GET /Users/:id` | [docs](https://www.ietf.org/rfc/rfc7644) |
| [List Groups](actions/list-groups.md) | `GET /Groups` | [docs](https://www.ietf.org/rfc/rfc7644) |
| [List Users](actions/list-users.md) | `GET /Users` | [docs](https://www.ietf.org/rfc/rfc7644) |
| [Reactivate User](actions/reactivate-user.md) | `PATCH /Users/:id` | [docs](https://www.ietf.org/rfc/rfc7644) |
| [Update Group](actions/update-group.md) | `PATCH /Groups/:id` | [docs](https://www.ietf.org/rfc/rfc7644) |
| [Update User](actions/update-user.md) | `PATCH /Users/:id` | [docs](https://www.ietf.org/rfc/rfc7644) |
