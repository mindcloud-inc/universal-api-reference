# Extensiv Order Manager: Create Standard Shipment

Creates a standard shipment in Extensiv Order Manager.

```
POST https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-standard-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extensiv Order Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-standard-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderIds[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-standard-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderIds[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `completeBatchAndDiscardFailedOrders` | boolean | no |  |
| `orderBatchNumber` | number | no |  |
| `orderIds[]` | array<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "message": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Validation errors returned by the API. |
| `message` | string | Bulk create result message. |
| `results` | array<object> | Bulk create result records. |

## Native endpoint

Through the native Extensiv Order Manager API, this operation is `PUT /v1.1/shipment/standard` (base URL `https://api.skubana.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-standard-shipment.md) for the provider-specific parameters and requirements.

