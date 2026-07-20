# QWIC Universal API Examples

These examples use the MindCloud API key and QWIC connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Bot Flow

Retrieves the flow for a QWIC bot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/fetch-bot-flow?connectionId=$CONNECTION_ID&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/fetch-bot-flow?${params}`, {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Fetch Bot Flow action reference](actions/fetch-bot-flow.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qWIC/latest/actions/fetch-bot-flow).

## Add Knowledge Base Domain Data Source

Adds a domain data source to a QWIC knowledge base.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/add-knowledge-base-domain-data-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "knowledgeBaseId": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/add-knowledge-base-domain-data-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "knowledgeBaseId": 1,
    "url": "https://example.com"
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Knowledge Base Domain Data Source action reference](actions/add-knowledge-base-domain-data-source.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qWIC/latest/actions/add-knowledge-base-domain-data-source).
