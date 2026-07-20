# WotNot Universal API Examples

These examples use the MindCloud API key and WotNot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bots

Retrieves bots from WotNot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/list-bots?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/list-bots?${params}`, {
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
      "bots": [
        {}
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

See the full [List Bots action reference](actions/list-bots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wotNot/latest/actions/list-bots).

## Add Knowledge Base Domain Source

Adds a domain source to a WotNot knowledge base.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/add-knowledge-base-domain-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "knowledgeBaseId": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/add-knowledge-base-domain-source', {
  method: 'PUT',
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
      "domain_id": 1,
      "ok": true,
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Knowledge Base Domain Source action reference](actions/add-knowledge-base-domain-source.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wotNot/latest/actions/add-knowledge-base-domain-source).
