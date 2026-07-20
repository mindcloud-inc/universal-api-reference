# Stackby: Update Row

Updates an existing row in a Stackby table.

```
PUT https://connect.mindcloud.co/v1/universal/stackby/latest/actions/update-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stackby/latest/actions/update-row" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackby/latest/actions/update-row', {
  method: 'PUT',
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
| `records` | list<object> | yes | Records array containing one row id and field patch. |

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
| `field` | object | Updated row field values keyed by column name. |
| `id` | string | Updated row ID. |

## Native endpoint

Through the native Stackby API, this operation is `PATCH /betav1/rowupdate/{{stackId}}/{{tableName}}` (base URL `https://stackby.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-row.md) for the provider-specific parameters and requirements.

