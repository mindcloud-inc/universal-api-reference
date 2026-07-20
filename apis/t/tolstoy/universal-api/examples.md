# Tolstoy Universal API Examples

These examples use the MindCloud API key and Tolstoy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Videos

Retrieves all video records from Tolstoy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/list-videos?${params}`, {
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
      "videos": [
        {
          "createdAt": "string",
          "gifSize": "string",
          "gifUrl": "https://example.com",
          "id": "string",
          "name": "Ava Chen",
          "posterGifUrl": "https://example.com",
          "videoUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Videos action reference](actions/list-videos.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tolstoy/latest/actions/list-videos).

## Add Webhook

Creates a new webhook in Tolstoy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/add-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tolstoy/latest/actions/add-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "string",
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
      "__typename": "Ava Chen",
      "appKey": "string",
      "createdAt": "string",
      "event": "string",
      "id": "string",
      "owner": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Webhook action reference](actions/add-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tolstoy/latest/actions/add-webhook).
