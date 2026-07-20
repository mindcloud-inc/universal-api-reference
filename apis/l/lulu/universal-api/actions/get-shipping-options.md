# Lulu: Get Shipping Options

Retrieves shipping options from Lulu.

```
GET https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-shipping-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-shipping-options?connectionId=$CONNECTION_ID&lineItems%5B%5D=%5Bobject%20Object%5D&shippingAddress=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lineItems[]": "[object Object]",
  "shippingAddress": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/get-shipping-options?${params}`, {
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
| `lineItems[]` | array | yes | Array of Lulu line items to price for shipping. Default: `[{"quantity":1,"page_count":32,"pod_package_id":"0600X0900.BW.STD.PB.060UW444.MXX"}]`. |
| `shippingAddress` | object | yes | Shipping address for the available shipping options lookup. Default: `{"city":"Washington","street1":"101 Independence Ave SE","postcode":"20540","state_code":"DC","country_code":"US","phone_number":"+12025550123"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "businessOnly": true,
          "costExclTax": "string",
          "currency": "string",
          "homeOnly": true,
          "id": 1,
          "level": "string",
          "maxDeliveryDate": "string",
          "maxDispatchDate": "string",
          "minDeliveryDate": "string",
          "minDispatchDate": "string",
          "postboxOk": true,
          "totalDaysMax": 1,
          "totalDaysMin": 1,
          "traceable": true,
          "transitTime": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<object> |  |
| `[].businessOnly` | boolean |  |
| `[].costExclTax` | string |  |
| `[].currency` | string |  |
| `[].homeOnly` | boolean |  |
| `[].id` | number |  |
| `[].level` | string |  |
| `[].maxDeliveryDate` | string |  |
| `[].maxDispatchDate` | string |  |
| `[].minDeliveryDate` | string |  |
| `[].minDispatchDate` | string |  |
| `[].postboxOk` | boolean |  |
| `[].totalDaysMax` | number |  |
| `[].totalDaysMin` | number |  |
| `[].traceable` | boolean |  |
| `[].transitTime` | number |  |

## Native endpoint

Through the native Lulu API, this operation is `POST /shipping-options/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipping-options.md) for the provider-specific parameters and requirements.

