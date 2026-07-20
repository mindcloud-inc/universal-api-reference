# Figma Universal API Examples

These examples use the MindCloud API key and Figma connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Component

Retrieves a component from Figma by key.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-component?connectionId=$CONNECTION_ID&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/figma/latest/actions/get-component?${params}`, {
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
      "error": true,
      "meta": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Component action reference](actions/get-component.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/figma/latest/actions/get-component).

## Create File Comment

Creates a new comment in a Figma file.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/figma/latest/actions/create-file-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileKey": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/figma/latest/actions/create-file-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileKey": "string",
    "message": "string"
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
      "clientMeta": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileKey": "string",
      "id": "string",
      "message": "string",
      "orderId": "string",
      "parentId": "string",
      "reactions": [
        {}
      ],
      "resolvedAt": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Create File Comment action reference](actions/create-file-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/figma/latest/actions/create-file-comment).
