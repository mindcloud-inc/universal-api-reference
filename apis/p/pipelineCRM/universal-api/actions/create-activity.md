# Pipeline CRM: Create Activity

Creates a new activity note in Pipeline CRM.

```
POST https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note.title` | string | no | The note title, if any. |
| `note.content` | string | no | The note content. |
| `note.userId` | number | no | The owner user ID of the note. |
| `note.dealId` | number | no | The deal ID associated with the note. |
| `note.companyId` | number | no | The company ID associated with the note. |
| `note.personId` | number | no | The person ID associated with the note. |
| `note.milestoneId` | number | no | The milestone ID associated with the note. |
| `note.noteCategoryId` | number | no | The category ID of the note. |
| `note.notifyUserIds[]` | array<number> | no | User IDs to notify when new comments are added. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "comments": {},
      "company_id": 1,
      "content": "string",
      "created_at": "string",
      "deal_id": 1,
      "id": 1,
      "is_sent_message": true,
      "milestone_id": 1,
      "note_category_id": 1,
      "note_category": {
        "id": 1,
        "name": "Ava Chen"
      },
      "notify_user_ids": [
        [
          "string"
        ]
      ],
      "person_id": 1,
      "possible_notify_user_ids": [
        [
          "string"
        ]
      ],
      "primary_association_id": 1,
      "primary_association_type": "string",
      "title": "string",
      "updated_at": "string",
      "user_id": 1,
      "user": {
        "avatar_thumb_url": "https://example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `comments` | object |  |
| `company_id` | number |  |
| `content` | string |  |
| `created_at` | string |  |
| `deal_id` | number |  |
| `id` | number |  |
| `is_sent_message` | boolean |  |
| `milestone_id` | number |  |
| `note_category_id` | number |  |
| `note_category.id` | number |  |
| `note_category.name` | string |  |
| `notify_user_ids[]` | array<string> |  |
| `person_id` | number |  |
| `possible_notify_user_ids[]` | array<string> |  |
| `primary_association_id` | number |  |
| `primary_association_type` | string |  |
| `title` | string |  |
| `updated_at` | string |  |
| `user_id` | number |  |
| `user.avatar_thumb_url` | string |  |
| `user.first_name` | string |  |
| `user.id` | number |  |
| `user.last_name` | string |  |

## Native endpoint

Through the native Pipeline CRM API, this operation is `POST /notes` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

