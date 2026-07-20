# <img src="https://images.mindcloud.co/apps/icons/images-3_1775073723420.jpeg" alt="Client Commander logo" width="28" height="28"> Client Commander: Universal API

Manage contacts, deals, tasks, activities, and users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/clientCommander/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.clientcommander.com/
- **Vendor API docs:** https://docs.clientcommander.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clientCommander/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Client Commander. |

