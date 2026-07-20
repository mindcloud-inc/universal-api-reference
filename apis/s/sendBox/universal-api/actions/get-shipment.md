# SendBox: Get Shipment



```
GET https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/get-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/get-shipment?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/get-shipment?${params}`, {
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
| `id` | number | yes | The shipment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "code": "string",
      "courier": {},
      "current_status": {},
      "date_created": "2026-05-07T12:00:00.000Z",
      "destination_address": "string",
      "destination_city": "string",
      "destination_contact_phone": "string",
      "destination_name": "Ava Chen",
      "destination_state": {},
      "fee": 1,
      "id": 1,
      "incoming_option": {},
      "items": [
        {}
      ],
      "last_updated": "2026-05-07T12:00:00.000Z",
      "merchant": {},
      "origin_address": "string",
      "origin_city": "string",
      "origin_country": {},
      "origin_phone": "string",
      "origin_state": {},
      "pk": "string",
      "possible_actions": [
        {}
      ],
      "status": {},
      "status_code": "string",
      "total_value": 1,
      "tracking": {},
      "tracking_code": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `code` | string |  |
| `courier` | object |  |
| `current_status` | object |  |
| `date_created` | date |  |
| `destination_address` | string |  |
| `destination_city` | string |  |
| `destination_contact_phone` | string |  |
| `destination_name` | string |  |
| `destination_state` | object |  |
| `fee` | number |  |
| `id` | number |  |
| `incoming_option` | object |  |
| `items` | array<object> |  |
| `last_updated` | date |  |
| `merchant` | object |  |
| `origin_address` | string |  |
| `origin_city` | string |  |
| `origin_country` | object |  |
| `origin_phone` | string |  |
| `origin_state` | object |  |
| `pk` | string |  |
| `possible_actions` | array<object> |  |
| `status` | object |  |
| `status_code` | string |  |
| `total_value` | number |  |
| `tracking` | object |  |
| `tracking_code` | string |  |
| `weight` | number |  |

## Native endpoint

Through the native SendBox API, this operation is `GET /shipping/shipments/:id` (base URL `https://live.sendbox.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment.md) for the provider-specific parameters and requirements.

