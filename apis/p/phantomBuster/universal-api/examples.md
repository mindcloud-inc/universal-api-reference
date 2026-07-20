# PhantomBuster Universal API Examples

These examples use the MindCloud API key and PhantomBuster connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Branches

Retrieves branches from PhantomBuster.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-branches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-branches?${params}`, {
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
      "createdAt": 1,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Branches action reference](actions/list-branches.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/phantomBuster/latest/actions/list-branches).

## Launch Agent

Launches an agent in PhantomBuster.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/launch-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/launch-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Launch Agent action reference](actions/launch-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/phantomBuster/latest/actions/launch-agent).
