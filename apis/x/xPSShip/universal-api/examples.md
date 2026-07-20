# XPS Ship Universal API Examples

These examples use the MindCloud API key and XPS Ship connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Services

Retrieves shipping services from XPS Ship.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/list-services?${params}`, {
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
      "carrierCode": "string",
      "carrierLabel": "string",
      "inbound": true,
      "packageTypes": [
        {}
      ],
      "serviceCode": "string",
      "serviceLabel": "string",
      "services": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Services action reference](actions/list-services.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xPSShip/latest/actions/list-services).

## Assign Tags to Order

Assigns tags to an order in XPS Ship.

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

Example response:

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

See the full [Assign Tags to Order action reference](actions/assign-tags-to-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xPSShip/latest/actions/assign-tags-to-order).
