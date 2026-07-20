# Fivetran: Update Connection Column Config

Updates column configuration for a connection schema in Fivetran.

```
PUT https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-connection-column-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-connection-column-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "string",
  "columnName": "Ava Chen",
  "enabled": true,
  "schemaName": "Ava Chen",
  "tableName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-connection-column-config', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "columnName": "Ava Chen",
    "connectionId": "string",
    "enabled": true,
    "schemaName": "Ava Chen",
    "tableName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `columnName` | string | yes | The column name as stored in the connection schema config. |
| `connectionId` | string | yes | The unique identifier for the connection within Fivetran. |
| `enabled` | boolean | yes | Whether syncing the column into the destination is enabled. |
| `hashed` | boolean | no | Whether the column should be hashed. |
| `isPrimaryKey` | boolean | no | Whether the column is a primary key. |
| `schemaName` | string | yes | The schema name as stored in the connection schema config. |
| `tableName` | string | yes | The table name as stored in the connection schema config. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "hashed": true,
      "isPrimaryKey": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean |  |
| `hashed` | boolean |  |
| `isPrimaryKey` | boolean |  |

## Native endpoint

Through the native Fivetran API, this operation is `PATCH /connections/[:connectionId]/schemas/[:schemaName]/tables/[:tableName]/columns/[:columnName]` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-connection-column-config.md) for the provider-specific parameters and requirements.

