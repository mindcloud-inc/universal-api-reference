# Scaleway: Update Group

Updates an existing group in Scaleway.

```
PUT https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/update-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scaleway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/update-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scaleway/latest/actions/update-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes |  |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application_ids": [
        "string"
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "deletable": true,
      "description": "string",
      "editable": true,
      "id": "string",
      "managed": true,
      "name": "Ava Chen",
      "organization_id": "string",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application_ids` | array<string> |  |
| `created_at` | date |  |
| `deletable` | boolean |  |
| `description` | string |  |
| `editable` | boolean |  |
| `id` | string |  |
| `managed` | boolean |  |
| `name` | string |  |
| `organization_id` | string |  |
| `tags` | array<string> |  |
| `updated_at` | date |  |
| `user_ids` | array<string> |  |

## Native endpoint

Through the native Scaleway API, this operation is `PATCH /iam/v1alpha1/groups/:group_id` (base URL `https://api.scaleway.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group.md) for the provider-specific parameters and requirements.

