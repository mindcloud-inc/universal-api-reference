# Voiceflow: Get Transcript Evaluation

Retrieves a transcript evaluation from Voiceflow.

```
GET https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-transcript-evaluation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-transcript-evaluation?connectionId=$CONNECTION_ID&evaluationId=69c580ec37fdbf37359057ee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "evaluationId": "69c580ec37fdbf37359057ee"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-transcript-evaluation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `evaluationId` | string | yes | ID of the transcript evaluation to target. Example: `69c580ec37fdbf37359057ee`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "evaluation": {
        "averageCost": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "default": true,
        "description": "string",
        "enabled": true,
        "falsePrompt": "string",
        "id": "string",
        "name": "Ava Chen",
        "projectID": "string",
        "prompt": "string",
        "settings": {},
        "systemTag": "string",
        "truePrompt": "string",
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `evaluation.averageCost` | number | Average evaluation cost when available. |
| `evaluation.createdAt` | date | When the evaluation was created. |
| `evaluation.default` | boolean | Whether the evaluation is a default evaluation. |
| `evaluation.description` | string | Description of the evaluation. |
| `evaluation.enabled` | boolean | Whether the evaluation runs on new transcripts. |
| `evaluation.falsePrompt` | string | Prompt describing a false result. |
| `evaluation.id` | string | ID of the evaluation. |
| `evaluation.name` | string | Name of the evaluation. |
| `evaluation.projectID` | string | ID of the Voiceflow project. |
| `evaluation.prompt` | string | Prompt describing how the evaluation should be applied. |
| `evaluation.settings` | object | Optional model settings used by the evaluation. |
| `evaluation.systemTag` | string | Optional system tag for the evaluation. |
| `evaluation.truePrompt` | string | Prompt describing a true result. |
| `evaluation.type` | string | Evaluation type. |
| `evaluation.updatedAt` | date | When the evaluation was last updated. |

## Native endpoint

Through the native Voiceflow API, this operation is `GET https://analytics-api.voiceflow.com/v1/transcript-evaluation/:evaluationId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcript-evaluation.md) for the provider-specific parameters and requirements.

