# <img src="https://images.mindcloud.co/apps/icons/google-chat_1782742984133.png" alt="Google Chat logo" width="28" height="28"> Google Chat: Universal API

Send messages, manage spaces and memberships, and work with conversations in Google Chat.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleChat/latest
- **Category:** Communication / Team Messaging
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://workspace.google.com/products/chat/
- **Vendor API docs:** https://developers.google.com/workspace/chat/api/reference/rest

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Spaces](actions/list-spaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Channels

| Action | Method | Description |
| --- | --- | --- |
| [Find Direct Message](actions/find-direct-message.md) | GET | Finds an existing Google Chat direct message with a user. |
| [Get Space](actions/get-space.md) | GET | Retrieves details about a Google Chat space. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves Google Chat spaces the caller is a member of. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Get Membership](actions/get-membership.md) | GET | Retrieves details about a Google Chat membership. |
| [List Memberships](actions/list-memberships.md) | GET | Retrieves memberships in a Google Chat space. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a message in a Google Chat space. |

