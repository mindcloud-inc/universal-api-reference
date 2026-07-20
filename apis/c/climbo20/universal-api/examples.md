# Climbo 2.0 Universal API Examples

These examples use the MindCloud API key and Climbo 2.0 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Plans

Retrieves subscription plans from Climbo 2.0.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/list-plans?${params}`, {
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
      "amount": 1,
      "currency": "string",
      "id": "string",
      "interval": "string",
      "link": "https://example.com",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Plans action reference](actions/list-plans.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/climbo20/latest/actions/list-plans).

## Add Client

Creates a new client in Climbo 2.0.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/add-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "planId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/add-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "planId": "string"
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
      "businessName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "id": "string",
      "locationCount": 1,
      "planId": "string",
      "source": "string",
      "status": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Client action reference](actions/add-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/climbo20/latest/actions/add-client).
