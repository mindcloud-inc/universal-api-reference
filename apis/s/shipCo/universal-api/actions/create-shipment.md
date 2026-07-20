# Ship&Co: Create Shipment



```
POST https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/create-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "setup": {},
  "to_address": {},
  "from_address": {},
  "products[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/create-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "setup": {},
    "to_address": {},
    "from_address": {},
    "products[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `setup` | object | yes | Carrier, service, and shipping setup details. |
| `to_address` | object | yes | Recipient address object. |
| `from_address` | object | yes | Sender address object. |
| `products[]` | array<object> | yes | Product line items array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parcels[]` | array<object> | no | Parcel details array for international shipping. |
| `customs` | object | no | Customs details for international shipments. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "delivery": {},
      "from_address": {},
      "id": "string",
      "products": [
        {}
      ],
      "state": "string",
      "to_address": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Shipment creation timestamp. |
| `delivery` | object | Carrier, tracking number, label, and invoice details. |
| `from_address` | object | Sender address. |
| `id` | string | Shipment ID. |
| `products` | array<object> | Product line items. |
| `state` | string | Shipment state. |
| `to_address` | object | Recipient address. |

## Native endpoint

Through the native Ship&Co API, this operation is `POST /shipments` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment.md) for the provider-specific parameters and requirements.

