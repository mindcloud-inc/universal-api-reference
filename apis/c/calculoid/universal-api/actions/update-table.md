# Calculoid: Update Table



```
PUT https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/update-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/update-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calculatorId": "109359",
  "tableId": "42",
  "name": "Pricing Table",
  "data": "col_a,col_b\\n1,2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/update-table', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calculatorId": "109359",
    "tableId": "42",
    "name": "Pricing Table",
    "data": "col_a,col_b\\n1,2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calculatorId` | string | yes | Calculoid calculator ID. Default: `0`. Example: `109359`. |
| `tableId` | string | yes | Calculoid table ID. Default: `0`. Example: `42`. |
| `name` | string | yes | Updated table name. Default: `MindCloud safe test table`. Example: `Pricing Table`. |
| `data` | string | yes | Updated table CSV data or structured data payload. Default: `key,value\nsample,1`. Example: `col_a,col_b\n1,2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alerts": [
        {
          "msg": "string",
          "type": "string"
        }
      ],
      "table": {
        "data": "string",
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts[].msg` | string |  |
| `alerts[].type` | string |  |
| `table.data` | string |  |
| `table.id` | number |  |
| `table.name` | string |  |

## Native endpoint

Through the native Calculoid API, this operation is `POST /calculator/:calculatorId/tables/:tableId/edit` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-table.md) for the provider-specific parameters and requirements.

