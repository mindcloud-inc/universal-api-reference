# Rocketadmin: List Table Filters



```
GET https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/list-table-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketadmin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/list-table-filters?connectionId=$CONNECTION_ID&connectionId=string&tableName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string",
  "tableName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/list-table-filters?${params}`, {
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
| `tableName` | string | yes | Rocketadmin table name for the saved filter set. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "dynamic_column": {
        "column_name": "Ava Chen",
        "comparator": "string"
      },
      "filters": {},
      "id": "string",
      "name": "Ava Chen",
      "table_name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `dynamic_column` | object |  |
| `dynamic_column.column_name` | string |  |
| `dynamic_column.comparator` | string |  |
| `filters` | object |  |
| `id` | string |  |
| `name` | string |  |
| `table_name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Rocketadmin API, this operation is `GET /table-filters/:connectionId/all` (base URL `https://app.rocketadmin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-table-filters.md) for the provider-specific parameters and requirements.

