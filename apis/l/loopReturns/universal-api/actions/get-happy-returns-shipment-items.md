# Loop Returns: Get Happy Returns Shipment Items



```
GET https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/get-happy-returns-shipment-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loop Returns `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/get-happy-returns-shipment-items?connectionId=$CONNECTION_ID&shipmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopReturns/latest/actions/get-happy-returns-shipment-items?${params}`, {
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
| `page` | number | no | Example: `1`. |
| `shipmentId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Loop Returns API returns.

## Native endpoint

Through the native Loop Returns API, this operation is `GET /happy-returns/shipments/:shipmentId/items` (base URL `https://api.loopreturns.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-happy-returns-shipment-items.md) for the provider-specific parameters and requirements.

