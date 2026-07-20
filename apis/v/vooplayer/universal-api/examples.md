# Vooplayer Universal API Examples

These examples use the MindCloud API key and Vooplayer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from your Vooplayer account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/list-projects?${params}`, {
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
      "archived": 1,
      "created": "string",
      "id": 1,
      "name": "Ava Chen",
      "numberOfGB": 1,
      "numberOfSeconds": 1,
      "numberOfVideos": 1,
      "settings": 1,
      "theme": 1,
      "updated": "string",
      "userID": 1,
      "v3ID": 1
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vooplayer/latest/actions/list-projects).

## Add Whitelisted Domain

Creates a whitelisted domain in Vooplayer.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/add-whitelisted-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/add-whitelisted-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
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

See the full [Add Whitelisted Domain action reference](actions/add-whitelisted-domain.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vooplayer/latest/actions/add-whitelisted-domain).
