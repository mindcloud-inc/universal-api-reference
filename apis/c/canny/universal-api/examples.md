# Canny Universal API Examples

These examples use the MindCloud API key and Canny connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Boards

Retrieves all available boards from Canny.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canny/latest/actions/list-boards?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isPrivate": true,
      "name": "Ava Chen",
      "postCount": 1,
      "privateComments": true,
      "token": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Boards action reference](actions/list-boards.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/canny/latest/actions/list-boards).

## Change Post Category

Updates a post category in Canny.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/canny/latest/actions/change-post-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "postID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canny/latest/actions/change-post-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "postID": "string"
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
      "author": {},
      "board": {},
      "by": {},
      "category": {},
      "clickup": {},
      "commentCount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "details": "string",
      "eta": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "idea": {},
      "imageURLs": [
        "https://example.com"
      ],
      "jira": {},
      "linear": {},
      "mergeHistory": [
        {}
      ],
      "owner": {},
      "roadmaps": [
        {}
      ],
      "score": 1,
      "status": "string",
      "statusChangedAt": "2026-05-07T12:00:00.000Z",
      "tags": [
        {}
      ],
      "title": "string",
      "totalMRR": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Change Post Category action reference](actions/change-post-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/canny/latest/actions/change-post-category).
