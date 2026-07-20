# LoopedIn Universal API Examples

These examples use the MindCloud API key and LoopedIn connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves workspaces from LoopedIn.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-workspaces?${params}`, {
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
      "account": "string",
      "created": "string",
      "guid": "string",
      "id": "string",
      "roadmap": "string",
      "slug": "string",
      "title": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loopedIn/latest/actions/list-workspaces).

## Create Feedback

Creates a new feedback item in LoopedIn.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "board": "string",
  "category": "string",
  "title": "string",
  "workspace_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "board": "string",
    "category": "string",
    "title": "string",
    "workspace_id": "string"
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
      "account": "string",
      "board": "string",
      "category": "string",
      "completed": true,
      "created": "string",
      "createdBy": "string",
      "description": "string",
      "id": "string",
      "public": true,
      "title": "string",
      "updated": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Feedback action reference](actions/create-feedback.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/loopedIn/latest/actions/create-feedback).
