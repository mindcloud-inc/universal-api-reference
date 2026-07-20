# Rocketadmin: Get Table Row By Primary Key



```
GET https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-table-row-by-primary-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketadmin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-table-row-by-primary-key?connectionId=$CONNECTION_ID&connectionId=string&tableName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string",
  "tableName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-table-row-by-primary-key?${params}`, {
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

Through the native Rocketadmin API, this operation is `GET /table/row/:connectionId` (base URL `https://app.rocketadmin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-row-by-primary-key.md) for the provider-specific parameters and requirements.

