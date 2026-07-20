# BaseLinker: Get Order Payments History

Retrieves payment history for an order in BaseLinker.

```
GET https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-order-payments-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-order-payments-history?connectionId=$CONNECTION_ID&order_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "order_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-order-payments-history?${params}`, {
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
| `order_id` | number | yes | Order identifier from BaseLinker order manager. |
| `show_full_history` | boolean | no | Include full payment history, including manual edits and value changes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BaseLinker API returns.

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-payments-history.md) for the provider-specific parameters and requirements.

