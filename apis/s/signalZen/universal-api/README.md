# <img src="https://images.mindcloud.co/apps/icons/signalzen-logo-512x512_1775168553673.png" alt="SignalZen logo" width="28" height="28"> SignalZen: Universal API

SignalZen is a customer support platform for managing website conversations, users, and support messages from Slack, Microsoft Teams, email, and the SignalZen console.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/signalZen/latest
- **Category:** Support / Ticketing
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.signalzen.com
- **Vendor API docs:** https://docs.signalzen.com/docs/category/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalZen/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Get User Message](actions/get-user-message.md) | GET | Retrieves a user's message from SignalZen. |
| [List User Messages](actions/list-user-messages.md) | GET | Retrieves a user's messages from SignalZen. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from SignalZen. |
| [List Users](actions/list-users.md) | GET | Retrieves users from SignalZen. |

