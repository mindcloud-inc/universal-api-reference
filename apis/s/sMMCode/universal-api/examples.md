# SMMCode Universal API Examples

These examples use the MindCloud API key and SMMCode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Services



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/list-services?${params}`, {
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
      "category": "string",
      "max": "string",
      "min": "string",
      "name": "Ava Chen",
      "rate": "string",
      "service": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Services action reference](actions/list-services.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMMCode/latest/actions/list-services).

## Add Order



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/add-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "service": "string",
  "link": "https://example.com",
  "quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/add-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "service": "string",
    "link": "https://example.com",
    "quantity": 1
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
      "order": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Order action reference](actions/add-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMMCode/latest/actions/add-order).
