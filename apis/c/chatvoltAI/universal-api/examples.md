# Chatvolt AI Universal API Examples

These examples use the MindCloud API key and Chatvolt AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from Chatvolt AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/contacts-get?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/contacts-get?${params}`, {
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
      "contacts": [
        "string"
      ],
      "count": 1
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/contacts-get.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatvoltAI/latest/actions/contacts-get).

## Add Number to Whitelist

Adds a whitelist number in Chatvolt AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-add-whitelist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "whatsappNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-add-whitelist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "whatsappNumber": "string"
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
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Number to Whitelist action reference](actions/agents-add-whitelist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chatvoltAI/latest/actions/agents-add-whitelist).
