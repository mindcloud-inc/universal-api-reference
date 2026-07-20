# Cratejoy: Get Shipment

Retrieves a shipment from Cratejoy.

```
GET https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/get-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/get-shipment?connectionId=$CONNECTION_ID&shipId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/get-shipment?${params}`, {
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
| `shipId` | number | yes | The Cratejoy shipment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adjusted_ordered_at": "2026-05-07T12:00:00.000Z",
      "customer_id": 1,
      "id": 1,
      "shipped_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "target_at": "2026-05-07T12:00:00.000Z",
      "tracking_number": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adjusted_ordered_at` | date |  |
| `customer_id` | number |  |
| `id` | number |  |
| `shipped_at` | date |  |
| `status` | string |  |
| `target_at` | date |  |
| `tracking_number` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `GET /v1/shipments/:shipId/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment.md) for the provider-specific parameters and requirements.

