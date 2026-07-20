# OTO: Check OTO Delivery Fee

Checks OTO delivery fees in the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/check-oto-delivery-fee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/check-oto-delivery-fee?connectionId=$CONNECTION_ID&originCity=string&destinationCity=string&boxWidth=1&boxLength=1&boxHeight=1&boxWeight=1&boxName=Box1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "originCity": "string",
  "destinationCity": "string",
  "boxWidth": "1",
  "boxLength": "1",
  "boxHeight": "1",
  "boxWeight": "1",
  "boxName": "Box1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/check-oto-delivery-fee?${params}`, {
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
| `originCity` | string | yes | Origin city name. |
| `destinationCity` | string | yes | Destination city name. |
| `boxWidth` | number | yes | Width of the first box in the quote request. |
| `boxLength` | number | yes | Length of the first box in the quote request. |
| `boxHeight` | number | yes | Height of the first box in the quote request. |
| `boxWeight` | number | yes | Weight of the first box in the quote request. |
| `boxName` | string | yes | Name of the first box in the quote request. Default: `Box1`. |

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

Through the native OTO API, this operation is `POST /checkOTODeliveryFee` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-oto-delivery-fee.md) for the provider-specific parameters and requirements.

