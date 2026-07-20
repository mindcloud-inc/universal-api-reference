# Frameshift Universal API Examples

These examples use the MindCloud API key and Frameshift connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Activity Types

Retrieves a list of activity types from Frameshift.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-activity-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-activity-types?${params}`, {
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
      "data": [
        {
          "id": 1,
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Activity Types action reference](actions/list-activity-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/frameshift/latest/actions/list-activity-types).

## Create Comment

Creates a comment in a Frameshift conversation.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": 1,
  "conversation_id": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": 1,
    "conversation_id": 1,
    "text": "string"
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

See the full [Create Comment action reference](actions/create-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/frameshift/latest/actions/create-comment).
