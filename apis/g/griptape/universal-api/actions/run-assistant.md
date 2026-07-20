# Griptape: Run Assistant

Runs an assistant in Griptape.

```
POST https://connect.mindcloud.co/v1/universal/griptape/latest/actions/run-assistant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/run-assistant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assistantId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/griptape/latest/actions/run-assistant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assistantId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assistantId` | string | yes | The Griptape assistant ID to run. |
| `input` | string | no | Optional user input for the assistant run. |
| `threadId` | string | no | Optional thread ID to attach the run to. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stream` | boolean | no | Whether to return a live streamed Assistant Run response. |
| `ruleset_ids[]` | array<string> | no | Optional Ruleset IDs to attach to this Assistant Run. |
| `knowledge_base_ids[]` | array<string> | no | Optional Knowledge Base IDs to attach to this Assistant Run. |
| `structure_ids[]` | array<string> | no | Optional Structure IDs to attach to this Assistant Run. |
| `tool_ids[]` | array<string> | no | Optional Tool IDs to attach to this Assistant Run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "args": [
        "string"
      ],
      "assistant_id": "string",
      "assistant_run_id": "string",
      "completed_at": "string",
      "created_at": "string",
      "created_by": "string",
      "input": "string",
      "knowledge_base_ids": [
        "string"
      ],
      "model": "string",
      "organization_id": "string",
      "output": {},
      "retriever_ids": [
        "string"
      ],
      "ruleset_ids": [
        "string"
      ],
      "status": "string",
      "status_detail": "string",
      "stream": true,
      "structure_ids": [
        "string"
      ],
      "thread_id": "string",
      "tool_ids": [
        "string"
      ],
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `args` | array |  |
| `assistant_id` | string |  |
| `assistant_run_id` | string |  |
| `completed_at` | string |  |
| `created_at` | string |  |
| `created_by` | string |  |
| `input` | string |  |
| `knowledge_base_ids` | array<string> |  |
| `model` | string |  |
| `organization_id` | string |  |
| `output` | object |  |
| `retriever_ids` | array<string> |  |
| `ruleset_ids` | array<string> |  |
| `status` | string |  |
| `status_detail` | string |  |
| `stream` | boolean |  |
| `structure_ids` | array<string> |  |
| `thread_id` | string |  |
| `tool_ids` | array<string> |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `POST /api/assistants/:assistant_id/runs` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-assistant.md) for the provider-specific parameters and requirements.

