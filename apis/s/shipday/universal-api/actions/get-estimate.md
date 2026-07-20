# Shipday: Get Estimate

Retrieves an estimate from Shipday for an order.

```
GET https://connect.mindcloud.co/v1/universal/shipday/latest/actions/get-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/get-estimate?connectionId=$CONNECTION_ID&orderId=44865172" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "44865172"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipday/latest/actions/get-estimate?${params}`, {
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
| `orderId` | number | yes | Shipday order ID used in the request path. Example: `44865172`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryDuration": 1,
      "deliveryTime": "2026-05-07T12:00:00.000Z",
      "error": true,
      "errorCode": "string",
      "errorMessage": "string",
      "fee": 1,
      "id": "string",
      "name": "Ava Chen",
      "pickupDuration": 1,
      "pickupTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryDuration` | number | Estimated delivery duration in minutes. |
| `deliveryTime` | date | Estimated delivery timestamp. |
| `error` | boolean | Whether the provider returned an error. |
| `errorCode` | string | Provider error code when present. |
| `errorMessage` | string | Provider error message when present. |
| `fee` | number | Estimated fee for the delivery. |
| `id` | string | Provider identifier for the estimate row. |
| `name` | string | Provider name for the estimate row. |
| `pickupDuration` | number | Estimated pickup duration in minutes. |
| `pickupTime` | date | Estimated pickup timestamp. |

## Native endpoint

Through the native Shipday API, this operation is `GET /on-demand/estimate/:orderId` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-estimate.md) for the provider-specific parameters and requirements.

