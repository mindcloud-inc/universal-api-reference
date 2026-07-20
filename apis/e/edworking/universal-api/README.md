# <img src="https://images.mindcloud.co/apps/icons/edworking_1775671247179.png" alt="Edworking logo" width="28" height="28"> Edworking: Universal API

Edworking is an all-in-one productivity platform for tasks, chats, files, video calls, and team collaboration.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/edworking/latest
- **Category:** Productivity / Project Management
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://edworking.com
- **Vendor API docs:** https://edworking.com/api/overview/get-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Notifications](actions/list-notifications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edworking/latest/actions/list-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from Edworking, optionally filtered by project. |

