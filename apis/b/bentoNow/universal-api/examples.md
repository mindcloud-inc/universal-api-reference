# Bento Now Universal API Examples

These examples use the MindCloud API key and Bento Now connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Tags

Retrieves account tags from Bento Now.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/get-tags?${params}`, {
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
      "attributes": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "discardedAt": {},
        "name": "Ava Chen",
        "siteId": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Tags action reference](actions/get-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bentoNow/latest/actions/get-tags).

## Create Broadcasts

Creates a broadcast campaign in Bento Now.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-broadcasts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcasts[].content": "string",
  "broadcasts[].name": "Ava Chen",
  "broadcasts[].subject": "string",
  "broadcasts[].type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/create-broadcasts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcasts[].content": "string",
    "broadcasts[].name": "Ava Chen",
    "broadcasts[].subject": "string",
    "broadcasts[].type": "string"
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
      "failed": 1,
      "results": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Broadcasts action reference](actions/create-broadcasts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bentoNow/latest/actions/create-broadcasts).
