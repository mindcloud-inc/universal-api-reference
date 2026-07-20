# Quire Universal API Examples

These examples use the MindCloud API key and Quire connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Quire.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quire/latest/actions/get-current-user?${params}`, {
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
      "description": "string",
      "descriptionHtml": "string",
      "descriptionText": "string",
      "email": "ava@example.com",
      "iconColor": "string",
      "id": "string",
      "image": "string",
      "locale": "string",
      "name": "Ava Chen",
      "nameHtml": "Ava Chen",
      "nameText": "Ava Chen",
      "oid": "string",
      "timeZone": {},
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quire/latest/actions/get-current-user).

## Create Status

Creates a new status in Quire.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quire/latest/actions/create-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen",
  "value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quire/latest/actions/create-status', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen",
    "value": 1
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
      "color": "string",
      "name": "Ava Chen",
      "value": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Status action reference](actions/create-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quire/latest/actions/create-status).
