# XPS Ship: Delete Order

Deletes an existing order from XPS Ship.

```
DELETE https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/delete-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XPS Ship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/delete-order?connectionId=$CONNECTION_ID&integrationId=string&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "integrationId": "string",
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/delete-order?${params}`, {
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
| `integrationId` | string | yes | XPS Ship REST API integration ID. |
| `orderId` | string | yes | Unique order ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean | True when the order was deleted. |

## Native endpoint

Through the native XPS Ship API, this operation is `DELETE /restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId` (base URL `https://xpsshipper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-order.md) for the provider-specific parameters and requirements.

