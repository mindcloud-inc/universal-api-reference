# Eventix Universal API Examples

These examples use the MindCloud API key and Eventix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Events

Retrieves events from Eventix.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-events?connectionId=$CONNECTION_ID&type=normal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "normal"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-events?${params}`, {
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
      "auto-prune": true,
      "category": "string",
      "company_id": "string",
      "currency": "string",
      "description": "string",
      "guid": "string",
      "locale": "string",
      "location": {},
      "location_id": "string",
      "name": "Ava Chen",
      "retrievable_after": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subcategories": [
        "string"
      ],
      "type": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Events action reference](actions/get-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eventix/latest/actions/get-events).
