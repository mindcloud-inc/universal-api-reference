# Mailform: Get Order



```
GET https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=af91e239-0c5c-40b5-bab8-1f4271acba72" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "af91e239-0c5c-40b5-bab8-1f4271acba72"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-order?${params}`, {
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
| `orderId` | string | yes | ID of the order to retrieve. Example: `af91e239-0c5c-40b5-bab8-1f4271acba72`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mailform API returns.

## Native endpoint

Through the native Mailform API, this operation is `GET /orders/:order_id` (base URL `https://www.mailform.io/app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

