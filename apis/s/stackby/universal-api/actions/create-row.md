# Stackby: Create Row

Creates a new row in a Stackby table.

```
POST https://connect.mindcloud.co/v1/universal/stackby/latest/actions/create-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stackby/latest/actions/create-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackId": "string",
  "tableName": "Ava Chen",
  "records": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackby/latest/actions/create-row', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackId": "string",
    "tableName": "Ava Chen",
    "records": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stackId` | string | yes | Stack identifier from Stackby. |
| `tableName` | string | yes | Table name from Stackby. |
| `records` | list<object> | yes | Records array containing one field object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {},
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field` | object | Created row field values keyed by column name. |
| `id` | string | Created row ID. |

## Native endpoint

Through the native Stackby API, this operation is `POST /betav1/rowcreate/{{stackId}}/{{tableName}}` (base URL `https://stackby.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-row.md) for the provider-specific parameters and requirements.

