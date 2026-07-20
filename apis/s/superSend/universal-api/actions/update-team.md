# SuperSend: Update Team

Updates an existing team in SuperSend.

```
PUT https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Resource ID (UUID) |
| `name` | string | no |  |
| `domain` | string | no |  |
| `logo` | string | no |  |
| `about` | string | no |  |
| `meetingLink` | string | no |  |
| `meetingLinkText` | string | no |  |
| `autoPlacementTesting` | boolean | no |  |
| `autoPlacementTestingFrequency` | number | no | Allowed values: 7, 14, 30. |
| `notificationEmail` | string | no |  |
| `notificationEmailPreferences` | object | no | Per-category preferences for which notification types are sent to notification_email. Only provided keys are updated (merge). |
| `notificationEmailPreferences.errorNotificationsEmail` | boolean | no |  |
| `notificationEmailPreferences.successNotificationsEmail` | boolean | no |  |
| `notificationEmailPreferences.warmingNotificationsEmail` | boolean | no |  |
| `notificationEmailPreferences.newInboxActivityNotificationsEmail` | boolean | no |  |
| `notificationEmailPreferences.linkedinInboxActivityNotificationsEmail` | boolean | no |  |
| `notificationEmailPreferences.outOfContactsNotificationsEmail` | boolean | no |  |
| `inboxAutoTagSettings` | object | no |  |
| `inboxAutoTagSettings.autoTagBounced` | boolean | no |  |
| `inboxAutoTagSettings.autoTagOptOut` | boolean | no |  |
| `inboxAutoTagSettings.autoTagOutOfOffice` | boolean | no |  |
| `inboxSuperViews[]` | array<object> | no |  |
| `inboxSuperViews[].id` | string | no |  |
| `inboxSuperViews[].name` | string | no |  |
| `inboxSuperViews[].icon` | string | no |  |
| `inboxSuperViews[].filters` | object | no |  |
| `inboxSuperViews[].filters.mood` | string | no | Allowed values: positive, negative, neutral, needs_review. |
| `inboxSuperViews[].filters.statuses[]` | array<string> | no |  |
| `inboxSuperViews[].filters.lastMessageDirection` | string | no | Allowed values: inbound, outbound. |
| `inboxSuperViews[].filters.labels[]` | array<string> | no |  |
| `inboxSuperViews[].visible` | boolean | no |  |
| `inboxSuperViews[].order` | number | no | Range: 0 to inf. |

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

Through the native SuperSend API, this operation is `PATCH /teams/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team.md) for the provider-specific parameters and requirements.

