# Voiceflow: End Transcript

Marks a Voiceflow transcript as complete.

```
PUT https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/end-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/end-transcript" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transcriptId": "69c5805ff9294436f0b75ee0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/end-transcript', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transcriptId": "69c5805ff9294436f0b75ee0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transcriptId` | string | yes | ID of the transcript to target. Example: `69c5805ff9294436f0b75ee0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Confirmation that the transcript has ended. |

## Native endpoint

Through the native Voiceflow API, this operation is `POST https://analytics-api.voiceflow.com/v1/transcript/:transcriptId/project/:projectId/end` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/end-transcript.md) for the provider-specific parameters and requirements.

