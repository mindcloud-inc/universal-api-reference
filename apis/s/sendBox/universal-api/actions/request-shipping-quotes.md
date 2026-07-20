# SendBox: Request Shipping Quotes



```
GET https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/request-shipping-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/request-shipping-quotes?connectionId=$CONNECTION_ID&channel_code=api&currency=string&customs_option=string&destination=%5Bobject%20Object%5D&dimension=%5Bobject%20Object%5D&incoming_option=string&items=%5Bobject%20Object%5D&origin=%5Bobject%20Object%5D&package_type=string&pickup_date=2026-05-07T12%3A00%3A00.000Z&region=string&service_code=string&service_type=string&total_value=1&weight=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel_code": "api",
  "currency": "string",
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/request-shipping-quotes?${params}`, {
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
| `channel_code` | string | yes | Channel the request is being made from; set to api. Default: `api`. |
| `currency` | string | yes | Shop currency. |
| `customs_option` | string | yes | Customs options. |
| `destination` | object | yes | Recipient details object. |
| `dimension` | object | yes | Dimension details object. |
| `incoming_option` | string | yes | Incoming option; pickup or drop off. |
| `items` | list<object> | yes | Array of shipment item objects. |
| `origin` | object | yes | Sender details object. |
| `package_type` | string | yes | Package type. |
| `pickup_date` | date | yes | Date package is picked up. |
| `region` | string | yes | Region the package is shipped from. |
| `service_code` | string | yes | Can be standard, premium, or expedient. |
| `service_type` | string | yes | Set to either international or local. |
| `total_value` | number | yes | Value of shipment. |
| `weight` | number | yes | Weight of package. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connector_rates": [
        {}
      ],
      "currency": "string",
      "destination": {},
      "items": [
        {}
      ],
      "origin": {},
      "package_type": "string",
      "rate": {},
      "rate_type": "string",
      "rates": [
        {}
      ],
      "region": "string",
      "service_code": "string",
      "service_type": "string",
      "status": "string",
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connector_rates` | array<object> |  |
| `currency` | string |  |
| `destination` | object |  |
| `items` | array<object> |  |
| `origin` | object |  |
| `package_type` | string |  |
| `rate` | object |  |
| `rate_type` | string |  |
| `rates` | array<object> |  |
| `region` | string |  |
| `service_code` | string |  |
| `service_type` | string |  |
| `status` | string |  |
| `weight` | number |  |

## Native endpoint

Through the native SendBox API, this operation is `POST /shipping/shipment_delivery_quote` (base URL `https://live.sendbox.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-shipping-quotes.md) for the provider-specific parameters and requirements.

