# Fillout: Create Record

Creates a new record in Fillout.

```
POST https://connect.mindcloud.co/v1/universal/fillout/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "tableId": "string",
  "record": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillout/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "tableId": "string",
    "record": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The database identifier. |
| `tableId` | string | yes | The table identifier. |
| `record` | object | yes | The record payload to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "data": {},
      "fields": {},
      "id": "string",
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
| `data` | object |  |
| `fields` | object |  |
| `id` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Fillout API, this operation is `POST https://tables.fillout.com/api/v1/bases/:databaseId/tables/:tableId/records` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

