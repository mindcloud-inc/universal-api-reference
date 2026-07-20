# <img src="https://images.mindcloud.co/apps/icons/one-signal_1773346831267.png" alt="OneSignal logo" width="28" height="28"> OneSignal: Universal API

Send messages and manage users, segments, and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneSignal/latest
- **Category:** Marketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://onesignal.com
- **Vendor API docs:** https://documentation.onesignal.com/reference/rest-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Messages](actions/list-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSignal/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Alias

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Alias](actions/create-or-update-alias.md) | PUT | Creates or updates a user alias in OneSignal. |
| [Remove Alias](actions/remove-alias.md) | DELETE | Removes a user alias from OneSignal. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Export Audience Activity CSV](actions/export-audience-activity-csv.md) | GET | Exports audience activity as CSV from OneSignal. |
| [Get Message](actions/get-message.md) | GET | Retrieves message details from OneSignal. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from OneSignal. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Segment](actions/get-segment.md) | GET | Retrieves segment details from OneSignal. |
| [List Segments](actions/list-segments.md) | GET | Retrieves segments from OneSignal. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription by Alias](actions/create-subscription-by-alias.md) | POST | Creates a subscription in OneSignal by alias. |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes a subscription from OneSignal. |
| [Update Subscription by ID](actions/update-subscription-by-id.md) | PUT | Updates a subscription in OneSignal by ID. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a template in OneSignal. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes a template from OneSignal. |
| [Get Template](actions/get-template.md) | GET | Retrieves template details from OneSignal. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from OneSignal. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in OneSignal. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a user in OneSignal. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from OneSignal. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from OneSignal by alias. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in OneSignal. |

