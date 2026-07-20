# MindStudio Universal API Examples

These examples use the MindCloud API key and MindStudio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Load App

Retrieves app details from MindStudio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/load-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/load-app?${params}`, {
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
      "apps": [
        {}
      ],
      "orgId": "string",
      "orgName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Load App action reference](actions/load-app.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mindStudio/latest/actions/load-app).

## Generate Signed Access URL

Creates a signed access URL for a MindStudio agent.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/generate-signed-access-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindStudio/latest/actions/generate-signed-access-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
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
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Generate Signed Access URL action reference](actions/generate-signed-access-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mindStudio/latest/actions/generate-signed-access-url).
