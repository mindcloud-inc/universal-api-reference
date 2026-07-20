# Openlayer Universal API Examples

These examples use the MindCloud API key and Openlayer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves a list of projects from Openlayer.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-projects?${params}`, {
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
      "items": [
        {
          "dateCreated": "string",
          "dateUpdated": "string",
          "description": "string",
          "goalCount": 1,
          "id": "string",
          "inferencePipelineCount": 1,
          "links": {
            "app": "https://example.com"
          },
          "name": "Ava Chen",
          "sample": true,
          "taskType": "string",
          "versionCount": 1,
          "workspaceId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openlayer/latest/actions/list-projects).

## Create Inference Pipeline

Creates a new inference pipeline in Openlayer.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-inference-pipeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Validation Pipeline",
  "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248",
  "storageType": "local"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-inference-pipeline', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Validation Pipeline",
    "projectId": "2fcd0a42-23a7-44bb-b4fa-4fc3168fe248",
    "storageType": "local"
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
      "dateCreated": "string",
      "dateUpdated": "string",
      "description": "string",
      "id": "string",
      "links": {
        "app": "https://example.com"
      },
      "name": "Ava Chen",
      "paused": true,
      "projectId": "string",
      "status": "string",
      "storageType": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Inference Pipeline action reference](actions/create-inference-pipeline.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openlayer/latest/actions/create-inference-pipeline).
