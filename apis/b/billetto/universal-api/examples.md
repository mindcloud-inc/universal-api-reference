# Billetto Universal API Examples

These examples use the MindCloud API key and Billetto connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Public Events

Retrieves public events from Billetto.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetto/latest/actions/list-public-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetto/latest/actions/list-public-events?${params}`, {
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
      "data": [
        {}
      ],
      "has_more": true,
      "object": "string",
      "total": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Public Events action reference](actions/list-public-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billetto/latest/actions/list-public-events).

## Create Target Group Import

Creates a target group import in Billetto.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billetto/latest/actions/create-target-group-import" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billetto/latest/actions/create-target-group-import', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "id": "string",
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Target Group Import action reference](actions/create-target-group-import.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billetto/latest/actions/create-target-group-import).
