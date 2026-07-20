# SendBox: Track Shipment



```
GET https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/track-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/track-shipment?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/track-shipment?${params}`, {
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
| `code` | string | yes | The shipment tracking code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {},
      "amount_to_receive": 1,
      "code": "string",
      "courier": {},
      "date_created": "2026-05-07T12:00:00.000Z",
      "delivery_eta": "2026-05-07T12:00:00.000Z",
      "destination_address": "string",
      "destination_name": "Ava Chen",
      "events": [
        {}
      ],
      "id": 1,
      "last_updated": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "origin_address": "string",
      "origin_country": {},
      "origin_country_code": "string",
      "origin_name": "Ava Chen",
      "origin_state": {},
      "pickup_date": "2026-05-07T12:00:00.000Z",
      "status": {},
      "status_code": "string",
      "total_value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object |  |
| `amount_to_receive` | number |  |
| `code` | string |  |
| `courier` | object |  |
| `date_created` | date |  |
| `delivery_eta` | date |  |
| `destination_address` | string |  |
| `destination_name` | string |  |
| `events` | array<object> |  |
| `id` | number |  |
| `last_updated` | date |  |
| `notes` | string |  |
| `origin_address` | string |  |
| `origin_country` | object |  |
| `origin_country_code` | string |  |
| `origin_name` | string |  |
| `origin_state` | object |  |
| `pickup_date` | date |  |
| `status` | object |  |
| `status_code` | string |  |
| `total_value` | number |  |

## Native endpoint

Through the native SendBox API, this operation is `POST /shipping/tracking` (base URL `https://live.sendbox.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-shipment.md) for the provider-specific parameters and requirements.

