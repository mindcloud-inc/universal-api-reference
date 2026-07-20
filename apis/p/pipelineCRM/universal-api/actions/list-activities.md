# Pipeline CRM: List Activities

Finds activity notes in Pipeline CRM for a deal, person, or company.

```
GET https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/list-activities?${params}`, {
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
| `companyId` | number | no | Company association ID. |
| `dealId` | number | no | Deal association ID. |
| `personId` | number | no | Person association ID. |

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

Through the native Pipeline CRM API, this operation is `GET /notes` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

