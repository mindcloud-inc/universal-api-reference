# Shipcloud: Get Shipment

Retrieves a shipment from Shipcloud by ID.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-shipment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-shipment?${params}`, {
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
| `id` | string | yes | The Shipcloud shipment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "carrier_tracking_no": "string",
      "carrier_tracking_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "customs_declaration": {},
      "from": {},
      "id": "string",
      "label_url": "https://example.com",
      "packages": [
        {}
      ],
      "price": 1,
      "reference_number": "string",
      "service": "string",
      "shipper_notification_email": "ava@example.com",
      "to": {},
      "tracking_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `carrier_tracking_no` | string |  |
| `carrier_tracking_url` | string |  |
| `created_at` | date |  |
| `customs_declaration` | object |  |
| `from` | object |  |
| `id` | string |  |
| `label_url` | string |  |
| `packages` | array<object> |  |
| `price` | number |  |
| `reference_number` | string |  |
| `service` | string |  |
| `shipper_notification_email` | string |  |
| `to` | object |  |
| `tracking_url` | string |  |

## Native endpoint

Through the native Shipcloud API, this operation is `GET /shipments/:id` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment.md) for the provider-specific parameters and requirements.

