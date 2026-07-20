# Voiceflow: Create Transcript Evaluation

Creates a new transcript evaluation in Voiceflow.

```
POST https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-transcript-evaluation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-transcript-evaluation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud QA Evaluation",
  "enabled": "false",
  "prompt": "Determine whether the agent resolved the user request correctly.",
  "type": "boolean",
  "truePrompt": "The transcript shows the assistant resolved the issue or answered fully.",
  "falsePrompt": "The transcript shows the issue remains unresolved or the answer is incomplete."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/create-transcript-evaluation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud QA Evaluation",
    "enabled": "false",
    "prompt": "Determine whether the agent resolved the user request correctly.",
    "type": "boolean",
    "truePrompt": "The transcript shows the assistant resolved the issue or answered fully.",
    "falsePrompt": "The transcript shows the issue remains unresolved or the answer is incomplete."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the evaluation. Example: `MindCloud QA Evaluation`. |
| `enabled` | boolean | yes | Whether this evaluation runs on new transcripts. Default: `false`. Example: `false`. |
| `prompt` | string | yes | Prompt describing how the LLM should apply this evaluation. Example: `Determine whether the agent resolved the user request correctly.`. |
| `type` | string | yes | Type of evaluation. Default: `boolean`. Example: `boolean`. |
| `truePrompt` | string | yes | Prompt describing which transcripts should evaluate as true. Example: `The transcript shows the assistant resolved the issue or answered fully.`. |
| `falsePrompt` | string | yes | Prompt describing which transcripts should evaluate as false. Example: `The transcript shows the issue remains unresolved or the answer is incomplete.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional description of the evaluation. Example: `Binary QA evaluation for transcript testing.`. |
| `settings` | object | no | Optional model settings used when invoking this evaluation. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "evaluation": {
        "averageCost": {},
        "createdAt": "string",
        "default": true,
        "description": "string",
        "enabled": true,
        "falsePrompt": "string",
        "id": "string",
        "name": "Ava Chen",
        "projectID": "string",
        "prompt": "string",
        "settings": {},
        "systemTag": {},
        "truePrompt": "string",
        "type": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `evaluation.averageCost` | object |  |
| `evaluation.createdAt` | string |  |
| `evaluation.default` | boolean |  |
| `evaluation.description` | string |  |
| `evaluation.enabled` | boolean |  |
| `evaluation.falsePrompt` | string |  |
| `evaluation.id` | string |  |
| `evaluation.name` | string |  |
| `evaluation.projectID` | string |  |
| `evaluation.prompt` | string |  |
| `evaluation.settings` | object |  |
| `evaluation.systemTag` | object |  |
| `evaluation.truePrompt` | string |  |
| `evaluation.type` | string |  |
| `evaluation.updatedAt` | string |  |

## Native endpoint

Through the native Voiceflow API, this operation is `POST https://analytics-api.voiceflow.com/v1/transcript-evaluation` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcript-evaluation.md) for the provider-specific parameters and requirements.

