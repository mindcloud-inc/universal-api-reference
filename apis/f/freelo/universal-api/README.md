# <img src="https://images.mindcloud.co/apps/icons/favicon-www-freelo-io-48x48_1776106429061.png" alt="Freelo logo" width="28" height="28"> Freelo: Universal API

Manage projects, tasks, comments, and time tracking

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freelo/latest
- **Category:** Support / Ticketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.freelo.io
- **Vendor API docs:** https://api.freelo.io/docs/v1/freelo-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freelo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List All Projects](actions/list-all-projects.md) | GET | Retrieves all accessible projects from Freelo. |
| [List Projects](actions/list-projects.md) | GET | Retrieves own active projects from Freelo. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user from Freelo. |
| [List Users](actions/list-users.md) | GET | Retrieves visible coworkers from Freelo. |

