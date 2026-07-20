# WeSupply: Get Shipping Estimate For One Product

Retrieves a shipping estimate from WeSupply for one product.

```
GET https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-shipping-estimate-for-one-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-shipping-estimate-for-one-product?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-shipping-estimate-for-one-product?${params}`, {
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
| `locationType` | string | no | The lookup mode for the shipping estimate, such as zip code. |
| `requestId` | string | no | A caller-provided identifier for the shipping estimate request. |
| `zipCode` | string | no | The destination postal code for the shipping estimate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EstimatedDeliveryDate": "string",
      "EstimatedTimeMinutesE2E": 1,
      "LocationID": "string",
      "LocationType": "string",
      "RequestID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EstimatedDeliveryDate` | string |  |
| `EstimatedTimeMinutesE2E` | number |  |
| `LocationID` | string |  |
| `LocationType` | string |  |
| `RequestID` | string |  |

## Native endpoint

Through the native WeSupply API, this operation is `POST /shippingEstimate` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipping-estimate-for-one-product.md) for the provider-specific parameters and requirements.

