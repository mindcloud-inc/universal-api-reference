# Rocketadmin: List Table Rows



```
GET https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/list-table-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketadmin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/list-table-rows?connectionId=$CONNECTION_ID&connectionId=string&tableName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string",
  "tableName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/list-table-rows?${params}`, {
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
| `tableName` | string | yes | Rocketadmin table name within the selected connection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "currentPage": 1,
        "lastPage": 1,
        "perPage": 1,
        "total": 1
      },
      "rows": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `pagination.currentPage` | number |  |
| `pagination.lastPage` | number |  |
| `pagination.perPage` | number |  |
| `pagination.total` | number |  |
| `rows` | array<object> |  |
| `rows[].completed` | boolean |  |
| `rows[].course_id` | object |  |
| `rows[].course_id.id` | string |  |
| `rows[].course_id.title` | string |  |
| `rows[].enrolled_at` | string |  |
| `rows[].id` | string |  |
| `rows[].progress` | string |  |
| `rows[].user_id` | object |  |
| `rows[].user_id.full_name` | string |  |
| `rows[].user_id.id` | string |  |

## Native endpoint

Through the native Rocketadmin API, this operation is `GET /table/rows/:connectionId` (base URL `https://app.rocketadmin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-table-rows.md) for the provider-specific parameters and requirements.

