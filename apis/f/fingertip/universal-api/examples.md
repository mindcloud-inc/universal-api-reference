# Fingertip Universal API Examples

These examples use the MindCloud API key and Fingertip connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Health Check



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/get-health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/get-health-check?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Health Check action reference](actions/get-health-check.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fingertip/latest/actions/get-health-check).

## Create Block



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-block" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "name": "Ava Chen",
  "kind": "string",
  "componentBlockId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-block', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "name": "Ava Chen",
    "kind": "string",
    "componentBlockId": "string"
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

See the full [Create Block action reference](actions/create-block.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fingertip/latest/actions/create-block).
