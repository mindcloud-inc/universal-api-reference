# Calibre Universal API Examples

These examples use the MindCloud API key and Calibre connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites

Retrieves all available sites from Calibre.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-sites?${params}`, {
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
      "organisation": {
        "sitesList": {
          "nodes": [
            {
              "canonicalUrl": "https://example.com",
              "name": "Ava Chen",
              "slug": "string"
            }
          ],
          "totalCount": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calibre/latest/actions/list-sites).

## Create Deploy

Creates a new deploy in Calibre.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-deploy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.site": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-deploy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.site": "string"
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
      "createDeploy": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "repository": "string",
        "revision": "string",
        "url": "https://example.com",
        "username": "Ava Chen",
        "uuid": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Deploy action reference](actions/create-deploy.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/calibre/latest/actions/create-deploy).
