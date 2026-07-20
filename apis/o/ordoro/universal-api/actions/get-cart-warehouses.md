# Ordoro: Get Cart Warehouses

Retrieves warehouses for an Ordoro cart.

```
GET https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-cart-warehouses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ordoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-cart-warehouses?connectionId=$CONNECTION_ID&cartId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cartId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ordoro/latest/actions/get-cart-warehouses?${params}`, {
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
| `cartId` | string | yes | The Ordoro cart ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Ordoro API, this operation is `GET /cart/{cart_id}/warehouse/` (base URL `https://api.ordoro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cart-warehouses.md) for the provider-specific parameters and requirements.

