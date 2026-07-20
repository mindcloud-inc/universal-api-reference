# Voiceflow: Update Transcript Evaluation

Updates an existing transcript evaluation in Voiceflow.

```
PUT https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-transcript-evaluation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-transcript-evaluation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "evaluationId": "69c580ec37fdbf37359057ee"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-transcript-evaluation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "evaluationId": "69c580ec37fdbf37359057ee"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `evaluationId` | string | yes | ID of the transcript evaluation to target. Example: `69c580ec37fdbf37359057ee`. |
| `name` | string | no | Name of the evaluation. Example: `Wizard Temp Evaluation Updated`. |
| `description` | string | no | Description of the evaluation. Example: `Disposable evaluation updated during Wizard Stage 3 testing.`. |
| `enabled` | boolean | no | Whether the evaluation runs on every new transcript. Example: `true`. |
| `prompt` | string | no | Prompt describing how the evaluation should be applied. Example: `Classify whether the conversation shows qualified purchase intent.`. |
| `truePrompt` | string | no | Prompt describing which transcripts should evaluate as true. Example: `Return true when the user clearly asks to buy, schedule, or move forward soon.`. |
| `falsePrompt` | string | no | Prompt describing which transcripts should evaluate as false. Example: `Return false when the user is browsing, testing, or not signaling near-term intent.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `PATCH https://analytics-api.voiceflow.com/v1/transcript-evaluation/:evaluationId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-transcript-evaluation.md) for the provider-specific parameters and requirements.

