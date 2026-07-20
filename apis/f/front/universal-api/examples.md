# Front Universal API Examples

These examples use the MindCloud API key and Front connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get API Token Details

Retrieves API token details from Front.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/get-api-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/get-api-token-details?${params}`, {
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
      "id": [
        "string"
      ],
      "links": [
        {
          "self": [
            "https://example.com"
          ]
        }
      ],
      "name": [
        "Ava Chen"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get API Token Details action reference](actions/get-api-token-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/front/latest/actions/get-api-token-details).

## Add Comment

Creates a conversation comment in Front.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/front/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "cnv_123",
  "body": "Internal note for this conversation."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/front/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "cnv_123",
    "body": "Internal note for this conversation."
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
      "attachments": [
        "string"
      ],
      "author": {
        "customFields": {},
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "isAdmin": true,
        "isAvailable": true,
        "isBlocked": true,
        "lastName": "Chen",
        "links": {
          "related": {
            "conversations": "https://example.com",
            "inboxes": "https://example.com"
          },
          "self": "https://example.com"
        },
        "type": "string",
        "username": "Ava Chen"
      },
      "body": "string",
      "id": "string",
      "isPinned": true,
      "links": {
        "related": {
          "conversation": "https://example.com",
          "mentions": "https://example.com"
        },
        "self": "https://example.com"
      },
      "postedAt": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Comment action reference](actions/add-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/front/latest/actions/add-comment).
