# Clarifai: Create Workflow

Creates a new workflow in Clarifai.

```
POST https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "workflows[]": [
    {}
  ],
  "workflows[].id": "string",
  "workflows[].nodes[]": [
    {}
  ],
  "workflows[].nodes[].id": "string",
  "workflows[].nodes[].model": {},
  "workflows[].nodes[].model.id": "string",
  "workflows[].nodes[].model.user_id": "string",
  "workflows[].nodes[].model.app_id": "string",
  "workflows[].nodes[].model.model_version": {},
  "workflows[].nodes[].model.model_version.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "workflows[]": [{}],
    "workflows[].id": "string",
    "workflows[].nodes[]": [{}],
    "workflows[].nodes[].id": "string",
    "workflows[].nodes[].model": {},
    "workflows[].nodes[].model.id": "string",
    "workflows[].nodes[].model.user_id": "string",
    "workflows[].nodes[].model.app_id": "string",
    "workflows[].nodes[].model.model_version": {},
    "workflows[].nodes[].model.model_version.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clarifai app ID. |
| `workflows[]` | array<object> | yes | Workflows to create. |
| `workflows[].id` | string | yes | Workflow ID. |
| `workflows[].nodes[]` | array<object> | yes | Workflow nodes. |
| `workflows[].nodes[].id` | string | yes | Workflow node ID. |
| `workflows[].nodes[].model` | object | yes | Model used by the node. |
| `workflows[].nodes[].model.id` | string | yes | Model ID. |
| `workflows[].nodes[].model.user_id` | string | yes | Model owner user ID. |
| `workflows[].nodes[].model.app_id` | string | yes | Model app ID. |
| `workflows[].nodes[].model.model_version` | object | yes | Model version for the node. |
| `workflows[].nodes[].model.model_version.id` | string | yes | Model version ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clarifai API returns.

## Native endpoint

Through the native Clarifai API, this operation is `POST /v2/users/me/apps/:appId/workflows` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workflow.md) for the provider-specific parameters and requirements.

