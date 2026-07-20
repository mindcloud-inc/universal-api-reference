# Openlayer: Create Inference Pipeline

Creates a new inference pipeline in Openlayer.

```
POST https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/create-inference-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Inference pipeline description. Default: `Validation pipeline created by MindCloud for Openlayer app verification.`. |
| `name` | string | yes | Inference pipeline name. Default: `MindCloud Validation Pipeline`. |
| `paused` | boolean | no | Whether the pipeline starts paused. Default: `false`. |
| `projectId` | string | yes | Openlayer project ID. Default: `2fcd0a42-23a7-44bb-b4fa-4fc3168fe248`. |
| `storageType` | string | yes | Pipeline storage type. Default: `local`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string |  |
| `dateUpdated` | string |  |
| `description` | string |  |
| `id` | string |  |
| `links.app` | string |  |
| `name` | string |  |
| `paused` | boolean |  |
| `projectId` | string |  |
| `status` | string |  |
| `storageType` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `POST /projects/:projectId/inference-pipelines` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inference-pipeline.md) for the provider-specific parameters and requirements.

