# SuperSend: Get Team

Retrieves a team from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-team?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-team?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Resource ID (UUID) |

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
      "members": [
        {
          "email": "ava@example.com",
          "first_name": "Ava",
          "id": "string",
          "joined_at": "2026-05-07T12:00:00.000Z",
          "last_name": "Chen",
          "role": "string"
        }
      ],
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
| `members[].email` | string |  |
| `members[].first_name` | string |  |
| `members[].id` | string |  |
| `members[].joined_at` | date |  |
| `members[].last_name` | string |  |
| `members[].role` | string |  |
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

Through the native SuperSend API, this operation is `GET /teams/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

