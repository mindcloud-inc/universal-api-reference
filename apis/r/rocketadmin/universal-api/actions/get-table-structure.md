# Rocketadmin: Get Table Structure



```
GET https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-table-structure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketadmin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-table-structure?connectionId=$CONNECTION_ID&connectionId=string&tableName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string",
  "tableName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-table-structure?${params}`, {
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
      "foreignKeys": [
        {
          "column_name": "Ava Chen",
          "constraint_name": "Ava Chen",
          "referenced_column_name": "Ava Chen",
          "referenced_table_name": "Ava Chen"
        }
      ],
      "primaryColumns": [
        {
          "column_name": "Ava Chen",
          "data_type": "string"
        }
      ],
      "structure": [
        {
          "allow_null": true,
          "auto_increment": true,
          "column_default": "string",
          "column_name": "Ava Chen",
          "data_type": "string",
          "isExcluded": true,
          "isSearched": true
        }
      ],
      "table_widgets": [
        {
          "field_name": "Ava Chen",
          "id": "string",
          "name": "Ava Chen",
          "widget_type": "string"
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
| `foreignKeys` | array<object> |  |
| `foreignKeys[].column_name` | string |  |
| `foreignKeys[].constraint_name` | string |  |
| `foreignKeys[].referenced_column_name` | string |  |
| `foreignKeys[].referenced_table_name` | string |  |
| `primaryColumns` | array<object> |  |
| `primaryColumns[].column_name` | string |  |
| `primaryColumns[].data_type` | string |  |
| `structure` | array<object> |  |
| `structure[].allow_null` | boolean |  |
| `structure[].auto_increment` | boolean |  |
| `structure[].column_default` | string |  |
| `structure[].column_name` | string |  |
| `structure[].data_type` | string |  |
| `structure[].isExcluded` | boolean |  |
| `structure[].isSearched` | boolean |  |
| `table_widgets` | array<object> |  |
| `table_widgets[].field_name` | string |  |
| `table_widgets[].id` | string |  |
| `table_widgets[].name` | string |  |
| `table_widgets[].widget_type` | string |  |

## Native endpoint

Through the native Rocketadmin API, this operation is `GET /table/structure/:connectionId` (base URL `https://app.rocketadmin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-table-structure.md) for the provider-specific parameters and requirements.

