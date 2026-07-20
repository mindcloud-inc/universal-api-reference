# Stockpilot Universal API Examples

These examples use the MindCloud API key and Stockpilot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify API Credentials

Retrieves organization details for the current Stockpilot credentials.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/verify-api-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/verify-api-credentials?${params}`, {
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
      "features": {
        "accountingConnector": true,
        "apiAccess": true,
        "b2bPortal": true,
        "bestBeforeAlerts": true,
        "createPickingBatch": true,
        "emailCampaign": true,
        "odooConnector": true,
        "productFeed": true,
        "purchaseOrderManagement": true,
        "warehouseManagement": true
      },
      "id": 1,
      "organizationName": "Ava Chen",
      "uniqueId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify API Credentials action reference](actions/verify-api-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stockpilot/latest/actions/verify-api-credentials).

## Cancel Order

Updates an order as canceled in Stockpilot.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/cancel-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderPk": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/cancel-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderPk": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Cancel Order action reference](actions/cancel-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/stockpilot/latest/actions/cancel-order).
