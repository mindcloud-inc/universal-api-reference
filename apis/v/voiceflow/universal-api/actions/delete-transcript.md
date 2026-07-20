# Voiceflow: Delete Transcript

Deletes an existing transcript from Voiceflow.

```
DELETE https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-transcript?connectionId=$CONNECTION_ID&transcriptId=69c5805ff9294436f0b75ee0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "69c5805ff9294436f0b75ee0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/delete-transcript?${params}`, {
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
| `transcriptId` | string | yes | ID of the transcript to target. Example: `69c5805ff9294436f0b75ee0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `DELETE https://analytics-api.voiceflow.com/v1/transcript/:transcriptId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-transcript.md) for the provider-specific parameters and requirements.

