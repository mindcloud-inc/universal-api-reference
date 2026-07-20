# Gelato Universal API Examples

These examples use the MindCloud API key and Gelato connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Catalogs

Finds available product catalogs in Gelato.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/list-catalogs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gelato/latest/actions/list-catalogs?${params}`, {
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
      "catalogUid": "string",
      "productAttributes": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Catalogs action reference](actions/list-catalogs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gelato/latest/actions/list-catalogs).

## Cancel Order v2

Cancels an order in Gelato v2 by order reference ID.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/cancel-order-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderReferenceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gelato/latest/actions/cancel-order-v2', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderReferenceId": "string"
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

See the full [Cancel Order v2 action reference](actions/cancel-order-v2.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gelato/latest/actions/cancel-order-v2).
