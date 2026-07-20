# Phonely Universal API Examples

These examples use the MindCloud API key and Phonely connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Agent

Retrieves an agent from Phonely.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-agent?connectionId=$CONNECTION_ID&uid=string&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string",
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-agent?${params}`, {
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
      "agentId": "string",
      "name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Agent action reference](actions/get-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/phonely/latest/actions/get-agent).

## Add Agent Documents

Adds documents to a Phonely agent.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/add-agent-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "W4LT4yDethRPfyCn9YAEVeIqrDf1",
  "agentId": "nlBwoRo2blPKAKB29rQZ",
  "files": "https://example.com/knowledge.txt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phonely/latest/actions/add-agent-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "W4LT4yDethRPfyCn9YAEVeIqrDf1",
    "agentId": "nlBwoRo2blPKAKB29rQZ",
    "files": "https://example.com/knowledge.txt"
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
      "documentIds": [
        "string"
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Agent Documents action reference](actions/add-agent-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/phonely/latest/actions/add-agent-documents).
