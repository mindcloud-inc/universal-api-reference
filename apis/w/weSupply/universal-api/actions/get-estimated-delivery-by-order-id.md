# WeSupply: Get Estimated Delivery By Order ID

Retrieves estimated delivery details from WeSupply by order ID.

```
GET https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-estimated-delivery-by-order-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-estimated-delivery-by-order-id?connectionId=$CONNECTION_ID&orderExternalOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderExternalOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-estimated-delivery-by-order-id?${params}`, {
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
| `orderExternalOrderId` | string | yes | The external order identifier used in WeSupply to look up the delivery estimate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EstimateUTCOffset": 1,
      "EstimateUTCTimestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EstimateUTCOffset` | number | UTC offset in seconds for the delivery estimate window. |
| `EstimateUTCTimestamp` | string | Estimated delivery timestamp or timestamp range returned by WeSupply. |

## Native endpoint

Through the native WeSupply API, this operation is `POST /getEstimatedDeliveryByOrderId` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-estimated-delivery-by-order-id.md) for the provider-specific parameters and requirements.

