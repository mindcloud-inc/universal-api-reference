# <img src="https://images.mindcloud.co/apps/icons/chatforma_1775584276272.png" alt="Chatforma logo" width="28" height="28"> Chatforma: Universal API

Create chatbots, manage forms, and message bot users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chatforma/latest
- **Category:** Communication / Team Messaging
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.chatforma.com
- **Vendor API docs:** https://docs.chatforma.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Account](actions/get-current-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves current account authorization status from Chatforma. |

### Bot

| Action | Method | Description |
| --- | --- | --- |
| [List Bots](actions/list-bots.md) | GET | Retrieves chatbot bot records from Chatforma. |

### Bot Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot Variable](actions/create-bot-variable.md) | POST | Creates a new bot variable in Chatforma. |
| [Delete Bot Variable](actions/delete-bot-variable.md) | DELETE | Deletes an existing bot variable from Chatforma. |
| [List Bot Variables](actions/list-bot-variables.md) | GET | Retrieves bot variable records from Chatforma. |

### Dispatch

| Action | Method | Description |
| --- | --- | --- |
| [Create Dispatch To Segment](actions/create-dispatch-to-segment.md) | POST | Creates a segment dispatch in Chatforma. |
| [Create Dispatch To User](actions/create-dispatch-to-user.md) | POST | Creates a user dispatch in Chatforma. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Forms](actions/list-forms.md) | GET | Retrieves submitted form records from Chatforma. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Bot Messages](actions/list-bot-messages.md) | GET | Retrieves bot message records from Chatforma. |
| [List User Messages](actions/list-user-messages.md) | GET | Retrieves user message records from Chatforma. |
| [Send Existing Message To Segment](actions/send-existing-message-to-segment.md) | POST | Sends an existing message to a Chatforma segment. |
| [Send Existing Message To User](actions/send-existing-message-to-user.md) | POST | Sends an existing message to a Chatforma user. |
| [Send Message To Dialog User](actions/send-message-to-dialog-user.md) | POST | Creates a dialog message for a Chatforma user. |

### Notification Sample

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification Sample](actions/get-notification-sample.md) | GET | Retrieves notification sample fields from Chatforma. |

### Notification Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notification subscription records from Chatforma. |
| [Subscribe To Notifications](actions/subscribe-to-notifications.md) | POST | Creates a new notification subscription in Chatforma. |
| [Unsubscribe From Notifications](actions/unsubscribe-from-notifications.md) | DELETE | Deletes a notification subscription from Chatforma. |

### Segments

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET | Retrieves audience segment records from Chatforma. |

### User Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create User Variable](actions/create-user-variable.md) | POST | Creates a new user variable in Chatforma. |
| [Get User Variable](actions/get-user-variable.md) | GET | Retrieves user variable details from Chatforma. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Segment](actions/add-user-to-segment.md) | POST | Adds a user to a Chatforma segment. |
| [List Bot Users](actions/list-bot-users.md) | GET | Retrieves bot user records from Chatforma. |
| [List Open Dialog Users](actions/list-open-dialog-users.md) | GET | Retrieves users with open dialogs from Chatforma. |
| [List Segment Users](actions/list-segment-users.md) | GET | Retrieves users in a Chatforma segment. |
| [Remove User From Segment](actions/remove-user-from-segment.md) | DELETE | Deletes a user from a Chatforma segment. |

