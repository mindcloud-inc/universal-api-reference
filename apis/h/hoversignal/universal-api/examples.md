# Hoversignal Universal API Examples

These examples use the MindCloud API key and Hoversignal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test API Key Authentication



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/test-api-key-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/test-api-key-authentication?${params}`, {
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
      "siteDomain": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Test API Key Authentication action reference](actions/test-api-key-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hoversignal/latest/actions/test-api-key-authentication).

## Create Easter Egg Hook



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/create-easter-egg-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topic": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/create-easter-egg-hook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topic": "string",
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
      "id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Easter Egg Hook action reference](actions/create-easter-egg-hook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hoversignal/latest/actions/create-easter-egg-hook).
