# Starshipit: Delete Order



```
DELETE https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/delete-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/delete-order?connectionId=$CONNECTION_ID&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/delete-order?${params}`, {
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
| `orderId` | number | yes | The unique numeric identifier for the order |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `DELETE /orders/delete` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-order.md) for the provider-specific parameters and requirements.

