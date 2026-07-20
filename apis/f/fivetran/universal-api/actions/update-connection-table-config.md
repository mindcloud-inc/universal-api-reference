# Fivetran: Update Connection Table Config

Updates table configuration for a connection schema in Fivetran.

```
PUT https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-connection-table-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-connection-table-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "string",
  "enabled": true,
  "schemaName": "Ava Chen",
  "tableName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-connection-table-config', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `columns` | object | no | Column configuration object for the table. |
| `connectionId` | string | yes | The unique identifier for the connection within Fivetran. |
| `enabled` | boolean | yes | Whether syncing the table into the destination is enabled. |
| `schemaName` | string | yes | The schema name as stored in the connection schema config. |
| `tableName` | string | yes | The table name as stored in the connection schema config. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": {},
      "enabled": true,
      "syncMode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columns` | object |  |
| `enabled` | boolean |  |
| `syncMode` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `PATCH /connections/[:connectionId]/schemas/[:schemaName]/tables/[:tableName]` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-connection-table-config.md) for the provider-specific parameters and requirements.

