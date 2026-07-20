# Comfy.ICU: Run Workflow

Creates a new workflow run in Comfy.ICU.

```
POST https://connect.mindcloud.co/v1/universal/comfyICU/latest/actions/run-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Comfy.ICU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/comfyICU/latest/actions/run-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "6bAK1X_Y7QERnV30MZdo2",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/comfyICU/latest/actions/run-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "6bAK1X_Y7QERnV30MZdo2",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | string | yes | Comfy.ICU workflow ID from the workflow page or API code snippet. Example: `6bAK1X_Y7QERnV30MZdo2`. |
| `prompt` | string | yes | ComfyUI API-format workflow JSON prompt. Paste the full prompt JSON from Comfy.ICU's View API code output. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files` | string | no | Optional JSON object mapping ComfyUI destination paths to public file URLs for inputs, models, LoRAs, or embeddings. |
| `webhook` | string | no | Optional public endpoint Comfy.ICU should call with run status updates. Example: `https://your-public-web-server.com/api/comfyicu-webhook`. |
| `accelerator` | string | no | Optional GPU accelerator to use for the workflow run. One of: `0`, `1`, `2`, `3`, `4`, `5`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Comfy.ICU run ID returned when a workflow run is queued. |

## Native endpoint

Through the native Comfy.ICU API, this operation is `POST /api/v1/workflows/:workflow_id/runs` (base URL `https://comfy.icu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-workflow.md) for the provider-specific parameters and requirements.

