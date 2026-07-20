# Zoho Connect Universal API Examples

These examples use the MindCloud API key and Zoho Connect connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Networks

Retrieves all networks from Zoho Connect.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-networks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-networks?${params}`, {
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
      "id": "string",
      "isDefault": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "soid": "string",
      "url": "https://example.com",
      "zoid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get All Networks action reference](actions/get-all-networks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoConnect/latest/actions/get-all-networks).

## Add Comment

Creates a new comment in Zoho Connect.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeId": "string",
  "streamId": "string",
  "commentContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeId": "string",
    "streamId": "string",
    "commentContent": "string"
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
      "addComment": {
        "comment": {
          "canDelete": true,
          "canEdit": true,
          "canPinComment": true,
          "canTranslate": true,
          "commentType": "string",
          "content": "string",
          "formatedTime": "string",
          "id": "string",
          "isApproved": true,
          "streamId": "string",
          "streamType": "string",
          "time": "string",
          "url": "https://example.com",
          "userDetails": {
            "bgColor": "string",
            "canFollow": true,
            "id": "string",
            "imageUrl": "https://example.com",
            "name": "Ava Chen",
            "type": "string",
            "zuid": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Comment action reference](actions/add-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoConnect/latest/actions/add-comment).
