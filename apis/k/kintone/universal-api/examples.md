# Kintone Universal API Examples

These examples use the MindCloud API key and Kintone connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Apps

Retrieves apps from Kintone.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-apps?${params}`, {
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
      "apps": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Apps action reference](actions/list-apps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kintone/latest/actions/list-apps).

## Add Comment

Creates a comment on a Kintone record.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": 1,
  "recordId": 1,
  "commentText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kintone/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": 1,
    "recordId": 1,
    "commentText": "string"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Comment action reference](actions/add-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kintone/latest/actions/add-comment).
