# Jira Software Cloud Universal API Examples

These examples use the MindCloud API key and Jira Software Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Accessible Resources

Retrieves accessible Jira Software Cloud sites for this token.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/accessible-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/accessible-resources?${params}`, {
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
      "avatarUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "scopes": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Accessible Resources action reference](actions/accessible-resources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jiraSoftwareCloud/latest/actions/accessible-resources).

## Add Comment

Creates a new comment in Jira Software Cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "cloudId": "string",
  "issueIdOrKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "cloudId": "string",
    "issueIdOrKey": "string"
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
      "author": {
        "accountId": "string",
        "avatarUrls": {
          "48x48": "https://example.com"
        },
        "displayName": "Ava Chen",
        "emailAddress": "ava@example.com"
      },
      "body": {
        "content": [
          {
            "content": [
              {
                "text": "string"
              }
            ]
          }
        ]
      },
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "jsdPublic": true,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Comment action reference](actions/add-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jiraSoftwareCloud/latest/actions/add-comment).
