# ManyReach Universal API Examples

These examples use the MindCloud API key and ManyReach connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Mailing Lists

Retrieves mailing lists from ManyReach.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-mailing-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-mailing-lists?${params}`, {
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
      "folderId": 1,
      "listId": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Mailing Lists action reference](actions/list-mailing-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/manyReach/latest/actions/list-mailing-lists).

## Add Prospect Tag

Adds a tag to a prospect in ManyReach.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/add-prospect-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/add-prospect-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Prospect Tag action reference](actions/add-prospect-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/manyReach/latest/actions/add-prospect-tag).
