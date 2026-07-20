# Zakeke: Retrieve Order By Code



```
GET https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-order-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zakeke `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-order-by-code?connectionId=$CONNECTION_ID&orderCode=ORDER-1001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderCode": "ORDER-1001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zakeke/latest/actions/retrieve-order-by-code?${params}`, {
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
| `orderCode` | string | yes | Unique order identifier on the ecommerce. Example: `ORDER-1001`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zakeke API returns.

## Native endpoint

Through the native Zakeke API, this operation is `GET /v2/order/{orderCode}` (base URL `https://api.zakeke.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order-by-code.md) for the provider-specific parameters and requirements.

