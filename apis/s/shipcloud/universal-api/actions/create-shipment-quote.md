# Shipcloud: Create Shipment Quote

Creates a new shipment quote in Shipcloud.

```
POST https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-shipment-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-shipment-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/create-shipment-quote', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "shipment_quote": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shipment_quote` | object |  |

## Native endpoint

Through the native Shipcloud API, this operation is `POST /shipment_quotes` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment-quote.md) for the provider-specific parameters and requirements.

