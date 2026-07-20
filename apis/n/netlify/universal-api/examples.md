# Netlify Universal API Examples

These examples use the MindCloud API key and Netlify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-sites?${params}`, {
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
      "adminUrl": "https://example.com",
      "claimed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultDomain": "string",
      "deployUrl": "https://example.com",
      "id": "string",
      "managedDns": true,
      "name": "Ava Chen",
      "plan": "string",
      "siteId": "string",
      "ssl": true,
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/netlify/latest/actions/list-sites).

## Cancel Site Deploy



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/cancel-site-deploy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deployId": "69aac8135e01826d281456d7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netlify/latest/actions/cancel-site-deploy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deployId": "69aac8135e01826d281456d7"
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
      "context": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deployUrl": "https://example.com",
      "id": "string",
      "manualDeploy": true,
      "name": "Ava Chen",
      "siteId": "string",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Site Deploy action reference](actions/cancel-site-deploy.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/netlify/latest/actions/cancel-site-deploy).
