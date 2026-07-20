# SuperSend: Create Team

Creates a new team in SuperSend.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/create-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/create-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/create-team', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `domain` | string | no |  |
| `logo` | string | no |  |
| `about` | string | no |  |
| `meetingLink` | string | no |  |
| `meetingLinkText` | string | no |  |
| `autoPlacementTesting` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "about": "string",
      "auto_placement_testing": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "id": "string",
      "inbox_auto_tag_settings": {},
      "inbox_super_views": [
        {
          "filters": {
            "labels": [
              [
                "string"
              ]
            ],
            "lastMessageDirection": "string",
            "mood": "string",
            "statuses": [
              [
                "string"
              ]
            ]
          },
          "icon": "string",
          "id": "string",
          "name": "Ava Chen",
          "order": 1,
          "visible": true
        }
      ],
      "is_default": true,
      "logo": "string",
      "meeting_link": "https://example.com",
      "meeting_link_text": "https://example.com",
      "member_count": 1,
      "name": "Ava Chen",
      "notification_email": "ava@example.com",
      "notification_email_preferences": {
        "errorNotificationsEmail": true,
        "linkedinInboxActivityNotificationsEmail": true,
        "newInboxActivityNotificationsEmail": true,
        "outOfContactsNotificationsEmail": true,
        "successNotificationsEmail": true,
        "warmingNotificationsEmail": true
      },
      "organization": {
        "id": "string",
        "name": "Ava Chen"
      },
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | string |  |
| `auto_placement_testing` | boolean |  |
| `created_at` | date |  |
| `domain` | string |  |
| `id` | string |  |
| `inbox_auto_tag_settings` | object |  |
| `inbox_super_views[].filters.labels[]` | array<string> |  |
| `inbox_super_views[].filters.lastMessageDirection` | string |  |
| `inbox_super_views[].filters.mood` | string |  |
| `inbox_super_views[].filters.statuses[]` | array<string> |  |
| `inbox_super_views[].icon` | string |  |
| `inbox_super_views[].id` | string |  |
| `inbox_super_views[].name` | string |  |
| `inbox_super_views[].order` | number |  |
| `inbox_super_views[].visible` | boolean |  |
| `is_default` | boolean |  |
| `logo` | string |  |
| `meeting_link` | string |  |
| `meeting_link_text` | string |  |
| `member_count` | number |  |
| `name` | string |  |
| `notification_email` | string |  |
| `notification_email_preferences.errorNotificationsEmail` | boolean |  |
| `notification_email_preferences.linkedinInboxActivityNotificationsEmail` | boolean |  |
| `notification_email_preferences.newInboxActivityNotificationsEmail` | boolean |  |
| `notification_email_preferences.outOfContactsNotificationsEmail` | boolean |  |
| `notification_email_preferences.successNotificationsEmail` | boolean |  |
| `notification_email_preferences.warmingNotificationsEmail` | boolean |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `POST /teams` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team.md) for the provider-specific parameters and requirements.

