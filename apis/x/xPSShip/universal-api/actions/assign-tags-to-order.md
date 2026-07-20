# XPS Ship: Assign Tags to Order

Assigns tags to an order in XPS Ship.

```
PUT https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/assign-tags-to-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XPS Ship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/assign-tags-to-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "integrationId": "string",
  "orderId": "string",
  "tagIds": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/assign-tags-to-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "integrationId": "string",
    "orderId": "string",
    "tagIds": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `integrationId` | string | yes | XPS Ship REST API integration ID. |
| `orderId` | string | yes | Order ID to tag. |
| `tagIds` | list<string> | yes | Array of tag IDs to assign to the order. Accepts multiple values as an array. |

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
| `ok` | boolean | True when tags were assigned. |

## Native endpoint

Through the native XPS Ship API, this operation is `POST /restapi/v1/customers/:customerId/integrations/:integrationId/orders/:orderId/assign-tags` (base URL `https://xpsshipper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-tags-to-order.md) for the provider-specific parameters and requirements.

