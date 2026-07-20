# Xperiencify Universal API Examples

These examples use the MindCloud API key and Xperiencify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Courses

Retrieves courses from Xperiencify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-courses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/list-courses?${params}`, {
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
      "description": "string",
      "id": 1,
      "poster": "string",
      "slug": "string",
      "thumbnail": "string",
      "title": "string",
      "users": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Courses action reference](actions/list-courses.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xperiencify/latest/actions/list-courses).

## Add New Tag

Creates new tags in Xperiencify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-new-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagNames": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-new-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagNames": "Ava Chen"
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
      "tags": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add New Tag action reference](actions/add-new-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xperiencify/latest/actions/add-new-tag).
