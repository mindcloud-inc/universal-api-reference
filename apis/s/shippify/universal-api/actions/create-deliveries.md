# Shippify: Create Deliveries

Creates up to 100 deliveries in Shippify.

```
POST https://connect.mindcloud.co/v1/universal/shippify/latest/actions/create-deliveries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/create-deliveries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deliveries[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippify/latest/actions/create-deliveries', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deliveries[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | no | Optional Shippify company identifier where the deliveries will be created. |
| `type` | string | no | Optional Shippify delivery type such as slot, express, or flex. |
| `deliveries[]` | array<object> | yes | Required array of Shippify delivery payload objects using the documented pickup, dropoff, packages, referenceId, tags, extraData, and cod structure. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currencyCode": "string",
      "deliveryDate": "string",
      "distance": 1,
      "id": "string",
      "price": 1,
      "referenceId": "string",
      "statusDelivery": "string",
      "trackLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencyCode` | string | Currency code for the delivery price. |
| `deliveryDate` | string | Scheduled delivery datetime string returned by Shippify. |
| `distance` | number | Quoted delivery distance. |
| `id` | string | Created delivery identifier. |
| `price` | number | Quoted delivery price. |
| `referenceId` | string | Delivery reference identifier. |
| `statusDelivery` | string | Created delivery status. |
| `trackLink` | string | Tracking URL for the created delivery. |

## Native endpoint

Through the native Shippify API, this operation is `POST /v1/deliveries` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deliveries.md) for the provider-specific parameters and requirements.

