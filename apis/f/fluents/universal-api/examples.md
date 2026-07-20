# Fluents Universal API Examples

These examples use the MindCloud API key and Fluents connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agents

Retrieves agents from your Fluents account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluents/latest/actions/list-agents?${params}`, {
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
      "has_more": true,
      "items": [
        {}
      ],
      "page": 1,
      "size": 1,
      "total": 1,
      "total_is_estimated": true
    }
  ],
  "meta": {}
}
```

See the full [List Agents action reference](actions/list-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fluents/latest/actions/list-agents).

## Buy Number

Creates a new phone number purchase in Fluents.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/buy-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluents/latest/actions/buy-number', {
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
      "active": true,
      "config": {},
      "description": "string",
      "example_context": {},
      "id": "string",
      "inbound_agent": {},
      "is_routing_number": true,
      "label": "string",
      "number": "string",
      "outbound_only": true,
      "sms_enabled": true,
      "tags": [
        "string"
      ],
      "telephony_account_connection": "string",
      "telephony_provider": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Buy Number action reference](actions/buy-number.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fluents/latest/actions/buy-number).
