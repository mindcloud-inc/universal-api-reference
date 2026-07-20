# <img src="https://images.mindcloud.co/apps/icons/company-avatar-64ca5cf30a1ae-x2_1781290954132.png" alt="CallPage logo" width="28" height="28"> CallPage: Universal API

Manage CallPage widgets, users, calls, voice, and SMS

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/callPage/latest
- **Category:** Support / Contact Center
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.callpage.io/
- **Vendor API docs:** https://callpage.github.io/documentation-rest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Call Or Schedule](actions/call-or-schedule.md) | POST | Starts or schedules a widget call in CallPage. |
| [Get Call](actions/get-call.md) | GET | Retrieves a single call from CallPage. |
| [List Calls](actions/list-calls.md) | GET | Retrieves call history records from CallPage. |
| [Start Widget Call](actions/start-widget-call.md) | POST | Starts a widget call in CallPage. |
| [Update Call Field](actions/update-call-field.md) | PUT | Updates a field on an existing call in CallPage. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Users To Widget](actions/add-users-to-widget.md) | PUT | Adds users to an existing widget in CallPage. |
| [Create Manager](actions/create-manager.md) | POST | Creates a new manager in CallPage. |
| [Create SMS Message](actions/create-sms-message.md) | POST | Creates a new SMS message in CallPage. |
| [Create Voice Message](actions/create-voice-message.md) | POST | Creates a new voice message in CallPage. |
| [Create Widget](actions/create-widget.md) | POST | Creates a new widget in CallPage. |
| [Delete Manager](actions/delete-manager.md) | DELETE | Deletes an existing manager from CallPage. |
| [Delete Widget](actions/delete-widget.md) | DELETE | Deletes an existing widget from CallPage. |
| [Get Manager](actions/get-manager.md) | GET | Retrieves a single manager from CallPage. |
| [Get Widget](actions/get-widget.md) | GET | Retrieves a single widget from CallPage. |
| [List Managers](actions/list-managers.md) | GET | Retrieves all available managers from CallPage. |
| [List SMS Messages](actions/list-sms-messages.md) | GET | Retrieves all SMS messages from CallPage. |
| [List Voice Messages](actions/list-voice-messages.md) | GET | Retrieves all voice messages from CallPage. |
| [List Widgets](actions/list-widgets.md) | GET | Retrieves all available widgets from CallPage. |
| [Reset SMS Messages](actions/reset-sms-messages.md) | DELETE | Deletes all SMS messages from CallPage. |
| [Reset Voice Messages](actions/reset-voice-messages.md) | DELETE | Deletes all voice messages from CallPage. |
| [Update Manager](actions/update-manager.md) | PUT | Updates an existing manager in CallPage. |
| [Update SMS Message](actions/update-sms-message.md) | PUT | Updates an existing SMS message in CallPage. |
| [Update Voice Message](actions/update-voice-message.md) | PUT | Updates an existing voice message in CallPage. |
| [Update Widget](actions/update-widget.md) | PUT | Updates an existing widget in CallPage. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves all available users from CallPage. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in CallPage. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from CallPage. |
| [Get User](actions/get-user.md) | GET | Retrieves a single user from CallPage. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in CallPage. |

