# AdvantShop Universal API Examples

These examples use the MindCloud API key and AdvantShop connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Initialize Store

Retrieves store initialization data from AdvantShop.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/initialize-store?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/initialize-store?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "catalog": {},
      "currencies": [
        {}
      ],
      "customer": {},
      "settings": {}
    }
  ],
  "meta": {}
}
```

See the full [Initialize Store action reference](actions/initialize-store.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/advantShop/latest/actions/initialize-store).

## Change Order Status

Updates an order status in AdvantShop.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/change-order-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": 1,
  "statusId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/advantShop/latest/actions/change-order-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": 1,
    "statusId": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "result": true,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Change Order Status action reference](actions/change-order-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/advantShop/latest/actions/change-order-status).
