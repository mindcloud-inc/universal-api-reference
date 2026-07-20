# Umami Universal API Examples

These examples use the MindCloud API key and Umami connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Websites



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-websites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/list-websites?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "resetAt": "2026-05-07T12:00:00.000Z",
      "shareId": "string",
      "teamId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Websites action reference](actions/list-websites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/umami/latest/actions/list-websites).

## Create Website



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/umami/latest/actions/create-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umami/latest/actions/create-website', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "domain": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "replayConfig": {},
      "replayEnabled": true,
      "resetAt": "2026-05-07T12:00:00.000Z",
      "shareId": "string",
      "teamId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Website action reference](actions/create-website.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/umami/latest/actions/create-website).
