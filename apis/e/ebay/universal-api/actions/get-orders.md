# eBay: Get Orders



```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-orders?connectionId=$CONNECTION_ID&createTimeFrom=2026-06-01T00%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "createTimeFrom": "2026-06-01T00:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/get-orders?${params}`, {
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
| `createTimeFrom` | date | yes | Start of the order creation time window. eBay requires the CreateTimeFrom/CreateTimeTo range to be no more than 90 days. Example: `2026-06-01T00:00:00.000Z`. |
| `createTimeTo` | date | no | End of the order creation time window. eBay recommends sellers set this to current time minus 2 minutes. Example: `2026-06-18T12:00:00.000Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eBay API returns.

## Native endpoint

Through the native eBay API, this operation is `POST` (base URL `https://api.ebay.com/ws/api.dll`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-orders.md) for the provider-specific parameters and requirements.

