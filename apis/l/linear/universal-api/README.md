# <img src="https://images.mindcloud.co/apps/icons/linear_1771369933988.png" alt="Linear logo" width="28" height="28"> Linear: Universal API

Manage issues, plan projects, track cycles, and ship product faster.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linear/latest
- **Category:** Support / Ticketing
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** http://linear.app/
- **Vendor API docs:** https://linear.app/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linear/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Linear. |
| [Query](actions/query.md) | GET | Makes an authenticated raw GraphQL request to Linear. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Create Linear Issue. |
| [List Issues](actions/list-issues.md) | GET | Search Linear Issues. |
| [Update Issue](actions/update-issue.md) | GET | Update Linear Issue. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Linear. |

