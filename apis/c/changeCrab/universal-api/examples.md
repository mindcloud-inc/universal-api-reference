# ChangeCrab Universal API Examples

These examples use the MindCloud API key and ChangeCrab connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Changelog

Retrieves a changelog from ChangeCrab.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/get-changelog?connectionId=$CONNECTION_ID&id=e.g.%20product-updates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e.g. product-updates"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/get-changelog?${params}`, {
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
      "accent": "string",
      "accessid": "string",
      "autonotify": true,
      "created_at": "string",
      "domain": "string",
      "id": 1,
      "name": "Ava Chen",
      "private": true,
      "showbrand": true,
      "showfilters": true,
      "siteurl": "https://example.com",
      "subdomain": "string",
      "subscribeactive": true,
      "suggestion": true,
      "team": 1,
      "team_name": "Ava Chen",
      "teamdetails": {},
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Changelog action reference](actions/get-changelog.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/changeCrab/latest/actions/get-changelog).

## Create Changelog

Creates a new changelog in ChangeCrab.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/create-changelog" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "e.g. Product Updates",
  "team": "e.g. 101038"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/create-changelog', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "e.g. Product Updates",
    "team": "e.g. 101038"
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
      "accent": "string",
      "accessid": "string",
      "autonotify": true,
      "created_at": "string",
      "domain": "string",
      "id": 1,
      "name": "Ava Chen",
      "private": true,
      "showbrand": true,
      "showfilters": true,
      "siteurl": "https://example.com",
      "subdomain": "string",
      "subscribeactive": true,
      "suggestion": true,
      "team": 1,
      "team_name": "Ava Chen",
      "teamdetails": {},
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Changelog action reference](actions/create-changelog.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/changeCrab/latest/actions/create-changelog).
