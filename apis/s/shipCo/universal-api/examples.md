# Ship&Co Universal API Examples

These examples use the MindCloud API key and Ship&Co connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Shipments



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/list-shipments?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "delivery": {},
      "from_address": {},
      "id": "string",
      "state": "string",
      "to_address": {}
    }
  ],
  "meta": {}
}
```

See the full [List Shipments action reference](actions/list-shipments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipCo/latest/actions/list-shipments).

## Create Order



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "setup": {},
  "to_address": {},
  "products[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "setup": {},
    "to_address": {},
    "products[]": [{}]
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "from_address": {},
      "id": "string",
      "products": [
        {}
      ],
      "setup": {},
      "state": "string",
      "to_address": {},
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Order action reference](actions/create-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipCo/latest/actions/create-order).
