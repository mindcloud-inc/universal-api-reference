# Leantime Universal API Examples

These examples use the MindCloud API key and Leantime connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Project Types



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-project-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-project-types?${params}`, {
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
      "project": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Project Types action reference](actions/list-project-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leantime/latest/actions/list-project-types).

## Add Comment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.module": "project",
  "entityId": 1,
  "params.values.text": "string",
  "params.values.father": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leantime/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.module": "project",
    "entityId": 1,
    "params.values.text": "string",
    "params.values.father": "0"
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

See the full [Add Comment action reference](actions/add-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leantime/latest/actions/add-comment).
