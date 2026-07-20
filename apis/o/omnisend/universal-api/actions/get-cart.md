# Omnisend: Get Cart

Retrieves a cart from Omnisend.

```
GET https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/get-cart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnisend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/get-cart?connectionId=$CONNECTION_ID&cartID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cartID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/get-cart?${params}`, {
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
| `cartID` | string | yes | Omnisend cart ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omnisend API returns.

## Native endpoint

Through the native Omnisend API, this operation is `GET /v3/carts/:cartID` (base URL `https://api.omnisend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cart.md) for the provider-specific parameters and requirements.

