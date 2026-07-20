# SendBox: Create Shipment



```
POST https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/create-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel_code": "api",
  "destination": {},
  "incoming_option": "string",
  "items": {},
  "origin": {},
  "package_type": "string",
  "pickup_date": "2026-05-07T12:00:00.000Z",
  "region": "string",
  "service_code": "string",
  "total_value": 1,
  "weight": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/create-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel_code": "api",
    "destination": {},
    "incoming_option": "string",
    "items": {},
    "origin": {},
    "package_type": "string",
    "pickup_date": "2026-05-07T12:00:00.000Z",
    "region": "string",
    "service_code": "string",
    "total_value": 1,
    "weight": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callback_url` | string | no | Webhook URL to receive tracking updates. |
| `channel_code` | string | yes | Channel the request is being made from; set to api. Default: `api`. |
| `destination` | object | yes | Recipient details object. |
| `incoming_option` | string | yes | Incoming option; pickup or dropoff. |
| `items` | list<object> | yes | Array of shipment item objects. |
| `origin` | object | yes | Sender details object. |
| `package_type` | string | yes | Package type. |
| `pickup_date` | date | yes | Date package is picked up. |
| `region` | string | yes | Region the shipment is being shipped from. |
| `service_code` | string | yes | Can be international, nation-wide, or local. |
| `total_value` | number | yes | Value of shipment. |
| `weight` | number | yes | Weight of package. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "code": "string",
      "current_status": {},
      "date_created": "2026-05-07T12:00:00.000Z",
      "destination_city": "string",
      "destination_country": {},
      "destination_name": "Ava Chen",
      "destination_phone": "string",
      "destination_street": "string",
      "fee": 1,
      "has_waybill_error": true,
      "id": "string",
      "items": [
        {}
      ],
      "last_updated": "2026-05-07T12:00:00.000Z",
      "origin_city": "string",
      "origin_name": "Ava Chen",
      "origin_phone": "string",
      "origin_state": {},
      "origin_street": "string",
      "paid": 1,
      "payment_data": {},
      "pickup_courier": {},
      "pickup_date": "2026-05-07T12:00:00.000Z",
      "pk": "string",
      "possible_actions": [
        {}
      ],
      "region": "string",
      "selected_courier_id": "string",
      "status": {},
      "status_code": "string",
      "tracking_code": "string",
      "user_id": "string",
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
| `current_status` | object |  |
| `date_created` | date |  |
| `destination_city` | string |  |
| `destination_country` | object |  |
| `destination_name` | string |  |
| `destination_phone` | string |  |
| `destination_street` | string |  |
| `fee` | number |  |
| `has_waybill_error` | boolean |  |
| `id` | string |  |
| `items` | array<object> |  |
| `last_updated` | date |  |
| `origin_city` | string |  |
| `origin_name` | string |  |
| `origin_phone` | string |  |
| `origin_state` | object |  |
| `origin_street` | string |  |
| `paid` | number |  |
| `payment_data` | object |  |
| `pickup_courier` | object |  |
| `pickup_date` | date |  |
| `pk` | string |  |
| `possible_actions` | array<object> |  |
| `region` | string |  |
| `selected_courier_id` | string |  |
| `status` | object |  |
| `status_code` | string |  |
| `tracking_code` | string |  |
| `user_id` | string |  |
| `weight` | number |  |

## Native endpoint

Through the native SendBox API, this operation is `POST /shipping/shipments` (base URL `https://live.sendbox.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment.md) for the provider-specific parameters and requirements.

