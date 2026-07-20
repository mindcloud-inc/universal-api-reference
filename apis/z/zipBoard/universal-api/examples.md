# zipBoard Universal API Examples

These examples use the MindCloud API key and zipBoard connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organizations

Retrieves organizations from zipBoard.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-organizations?${params}`, {
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
      "Id": "string",
      "orgName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Organizations action reference](actions/get-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zipBoard/latest/actions/get-organizations).

## Create Feedback

Creates a new feedback comment in zipBoard.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "projectId": "string",
    "title": "string"
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
      "commentId": "string",
      "commentType": "string",
      "description": "string",
      "project_id": "string",
      "reply": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Feedback action reference](actions/create-feedback.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zipBoard/latest/actions/create-feedback).
