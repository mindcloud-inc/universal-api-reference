# Columns AI Universal API Examples

These examples use the MindCloud API key and Columns AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Visual Template

Retrieves a visual template from Columns AI by visual ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/get-visual-template?connectionId=$CONNECTION_ID&id=U6tALuJ3cTdPFw" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "U6tALuJ3cTdPFw"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/get-visual-template?${params}`, {
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
      "access": {},
      "createdAt": {},
      "creator": "string",
      "current": "string",
      "graph": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "shared": true,
      "thumb_base64": "string",
      "updatedAt": {},
      "version": 1,
      "versions": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Visual Template action reference](actions/get-visual-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/columnsAI/latest/actions/get-visual-template).

## Publish Graph

Publishes a graph to Columns AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/publish-graph" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "g-example",
  "name": "Quarterly Sales",
  "graph": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/columnsAI/latest/actions/publish-graph', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "g-example",
    "name": "Quarterly Sales",
    "graph": "[object Object]"
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

See the full [Publish Graph action reference](actions/publish-graph.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/columnsAI/latest/actions/publish-graph).
