# <img src="https://images.mindcloud.co/apps/icons/autentique-logo_1776705435203.png" alt="Autentique logo" width="28" height="28"> Autentique: Universal API

Autentique is an electronic signature platform for creating, sending, signing, and managing documents through its public GraphQL API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/autentique/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.autentique.com.br/en
- **Vendor API docs:** https://docs.autentique.com.br/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Current User](actions/fetch-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autentique/latest/actions/fetch-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Folders](actions/list-folders.md) | GET | Retrieves a list of folders from Autentique. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Organization](actions/get-current-organization.md) | GET | Retrieves the current organization from Autentique. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves a list of organizations from Autentique. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Current User](actions/fetch-current-user.md) | GET | Retrieves the current user from Autentique. |

