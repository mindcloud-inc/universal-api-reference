# SendBox: Calculate Landed Cost



```
GET https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/calculate-landed-cost
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/calculate-landed-cost?connectionId=$CONNECTION_ID&channel_code=api&customs_option=string&destination=%5Bobject%20Object%5D&dimension=%5Bobject%20Object%5D&incoming_option=string&items=%5Bobject%20Object%5D&origin=%5Bobject%20Object%5D&package_type=string&pickup_date=2026-05-07T12%3A00%3A00.000Z&region=string&service_code=string&service_type=string&total_value=1&weight=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel_code": "api",
  "customs_option": "string",
  "destination": "[object Object]",
  "dimension": "[object Object]",
  "incoming_option": "string",
  "items": "[object Object]",
  "origin": "[object Object]",
  "package_type": "string",
  "pickup_date": "2026-05-07T12:00:00.000Z",
  "region": "string",
  "service_code": "string",
  "service_type": "string",
  "total_value": "1",
  "weight": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/calculate-landed-cost?${params}`, {
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
| `callback_url` | string | no | Webhook URL for tracking updates. |
| `channel_code` | string | yes | Channel the request is being made from; set to api. Default: `api`. |
| `customs_option` | string | yes | Customs options. |
| `destination` | object | yes | Recipient details object. |
| `dimension` | object | yes | Dimension details object. |
| `incoming_option` | string | yes | Incoming option; pickup or drop off. |
| `items` | list<object> | yes | Array of shipment item objects. |
| `origin` | object | yes | Sender details object. |
| `package_type` | string | yes | Package type. |
| `pickup_date` | date | yes | Date package is picked up. |
| `region` | string | yes | Region the shipment is being shipped from. |
| `service_code` | string | yes | Can be international, nation-wide, or local. |
| `service_type` | string | yes | Service type. |
| `total_value` | number | yes | Value of shipment. |
| `weight` | number | yes | Weight of package. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "customs_option": "string",
      "destination": {},
      "dimension": {},
      "entity_id": "string",
      "estimate": {},
      "incoming_option": "string",
      "instance_id": "string",
      "items": [
        {}
      ],
      "origin": {},
      "package_type": "string",
      "pickup_date": "2026-05-07T12:00:00.000Z",
      "region": "string",
      "service_code": "string",
      "service_type": "string",
      "total_value": 1,
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
| `currency` | string |  |
| `customs_option` | string |  |
| `destination` | object |  |
| `dimension` | object |  |
| `entity_id` | string |  |
| `estimate` | object |  |
| `incoming_option` | string |  |
| `instance_id` | string |  |
| `items` | array<object> |  |
| `origin` | object |  |
| `package_type` | string |  |
| `pickup_date` | date |  |
| `region` | string |  |
| `service_code` | string |  |
| `service_type` | string |  |
| `total_value` | number |  |
| `user_id` | string |  |
| `weight` | number |  |

## Native endpoint

Through the native SendBox API, this operation is `POST /shipping/landed_cost_estimate` (base URL `https://live.sendbox.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-landed-cost.md) for the provider-specific parameters and requirements.

