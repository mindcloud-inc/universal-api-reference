# Voiceflow: Delete Transcript Evaluation

Deletes an existing transcript evaluation from Voiceflow.

```
DELETE https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-transcript-evaluation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-transcript-evaluation?connectionId=$CONNECTION_ID&evaluationId=69c580ec37fdbf37359057ee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "evaluationId": "69c580ec37fdbf37359057ee"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-transcript-evaluation?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `DELETE https://analytics-api.voiceflow.com/v1/transcript-evaluation/:evaluationId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-transcript-evaluation.md) for the provider-specific parameters and requirements.

