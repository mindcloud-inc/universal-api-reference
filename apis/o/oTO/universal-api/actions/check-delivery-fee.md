# OTO: Check Delivery Fee

Checks delivery fees in the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/check-delivery-fee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/check-delivery-fee?connectionId=$CONNECTION_ID&weight=string&totalDue=1&originCity=string&destinationCity=string&height=1&width=1&length=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "weight": "string",
  "totalDue": "1",
  "originCity": "string",
  "destinationCity": "string",
  "height": "1",
  "width": "1",
  "length": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/check-delivery-fee?${params}`, {
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
| `weight` | string | yes | Shipment weight used for the fee estimate. |
| `totalDue` | number | yes | COD or order total due amount. |
| `originCity` | string | yes | Origin city name. |
| `destinationCity` | string | yes | Destination city name. |
| `height` | number | yes | Package height. |
| `width` | number | yes | Package width. |
| `length` | number | yes | Package length. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryCompany": [
        {}
      ],
      "success": true,
      "traceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryCompany` | array<object> |  |
| `success` | boolean |  |
| `traceId` | string |  |

## Native endpoint

Through the native OTO API, this operation is `POST /checkDeliveryFee` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-delivery-fee.md) for the provider-specific parameters and requirements.

