# ZapCap: Create Task With Reference Transcript

Creates a caption task in ZapCap with a reference transcript.

```
POST https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/create-task-with-reference-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/create-task-with-reference-transcript" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": "string",
  "templateId": "string",
  "autoApprove": true,
  "referenceTranscript[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/create-task-with-reference-transcript', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": "string",
    "templateId": "string",
    "autoApprove": true,
    "referenceTranscript[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | string | yes | ZapCap video ID. |
| `templateId` | string | yes | ZapCap template ID. |
| `autoApprove` | boolean | yes | Automatically approve the transcript. |
| `referenceTranscript[]` | array<object> | yes | Phrase-level transcript entries with timing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string | Created ZapCap task ID. |

## Native endpoint

Through the native ZapCap API, this operation is `POST /videos/:videoId/task` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-with-reference-transcript.md) for the provider-specific parameters and requirements.

