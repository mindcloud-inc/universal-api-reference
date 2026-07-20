# Rye: Get Shipment

Retrieves a shipment from Rye.

```
GET https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-shipment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-shipment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The shipment id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkoutIntentId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "id": "string",
      "marketplaceOrderId": "string",
      "shippedAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "tracking": {},
      "trackingEvents": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkoutIntentId` | string |  |
| `createdAt` | date |  |
| `externalId` | string |  |
| `id` | string |  |
| `marketplaceOrderId` | string |  |
| `shippedAt` | date |  |
| `status` | string |  |
| `tracking` | object |  |
| `trackingEvents` | array<object> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Rye API, this operation is `GET /api/v1/shipments/{id}` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment.md) for the provider-specific parameters and requirements.

