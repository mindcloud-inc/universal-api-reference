# Billit: Delete Order

Deletes an existing order from Billit.

```
DELETE https://connect.mindcloud.co/v1/universal/billit/latest/actions/delete-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/billit/latest/actions/delete-order?connectionId=$CONNECTION_ID&orderID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billit/latest/actions/delete-order?${params}`, {
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
| `orderID` | number | yes | Billit OrderID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | boolean | True when the Billit order was deleted. |

## Native endpoint

Through the native Billit API, this operation is `DELETE /v1/orders/:orderID` (base URL `https://api.sandbox.billit.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-order.md) for the provider-specific parameters and requirements.

