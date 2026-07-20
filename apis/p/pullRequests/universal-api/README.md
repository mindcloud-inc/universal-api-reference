# <img src="https://images.mindcloud.co/apps/icons/pull-requests_1777392703438.png" alt="24 Pull Requests logo" width="28" height="28"> 24 Pull Requests: Universal API

Browse open source holiday contributions and participants

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pullRequests/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://24pullrequests.com
- **Vendor API docs:** https://24pullrequests.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Contribution

| Action | Method | Description |
| --- | --- | --- |
| [List Contributions](actions/list-contributions.md) | GET | Retrieves contributions from 24 Pull Requests. |

### Contributions Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Contributions Metadata](actions/get-contributions-metadata.md) | GET | Retrieves contribution counts and total pages from 24 Pull Requests. |

### Organisation

| Action | Method | Description |
| --- | --- | --- |
| [Get Organisation](actions/get-organisation.md) | GET | Retrieves an organisation from 24 Pull Requests. |
| [List Organisations](actions/list-organisations.md) | GET | Retrieves organisations from 24 Pull Requests. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves suggested projects from 24 Pull Requests. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from 24 Pull Requests. |
| [List Users](actions/list-users.md) | GET | Retrieves users from 24 Pull Requests. |

