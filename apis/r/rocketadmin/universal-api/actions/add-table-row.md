# Rocketadmin: Add Table Row



```
POST https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/add-table-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketadmin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/add-table-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "string",
  "tableName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/add-table-row', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionId": "string",
    "tableName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connectionId` | string | yes | Rocketadmin connection identifier from the path. |
| `tableName` | string | yes | Rocketadmin table name for the target row. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "course_id": {
        "id": "string",
        "title": "string"
      },
      "enrolled_at": "string",
      "id": "string",
      "progress": "string",
      "user_id": {
        "full_name": "Ava Chen",
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean |  |
| `course_id` | object |  |
| `course_id.id` | string |  |
| `course_id.title` | string |  |
| `enrolled_at` | string |  |
| `id` | string |  |
| `progress` | string |  |
| `user_id` | object |  |
| `user_id.full_name` | string |  |
| `user_id.id` | string |  |

## Native endpoint

Through the native Rocketadmin API, this operation is `POST /table/row/:connectionId` (base URL `https://app.rocketadmin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-table-row.md) for the provider-specific parameters and requirements.

