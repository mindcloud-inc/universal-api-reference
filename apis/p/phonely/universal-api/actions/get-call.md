# Phonely: Get Call

Retrieves a call from Phonely.

```
GET https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-call?connectionId=$CONNECTION_ID&uid=string&agentId=string&callId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string",
  "agentId": "string",
  "callId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/get-call?${params}`, {
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
| `uid` | string | yes | The Phonely user ID that owns the target call. |
| `agentId` | string | yes | The Phonely agent ID that received the call. |
| `callId` | string | yes | The Phonely call ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionItems": [
        "string"
      ],
      "agentName": "Ava Chen",
      "ai_success": true,
      "callDirection": "string",
      "callId": "string",
      "dashboardUrl": "https://example.com",
      "duration": 1,
      "endedReason": "string",
      "followUp": true,
      "keyPoints": [
        "string"
      ],
      "messages": [
        {}
      ],
      "purpose": "string",
      "recordingUrl": "https://example.com",
      "sentiment": "string",
      "summary": "string",
      "topic": [
        "string"
      ],
      "transcript": [
        {}
      ],
      "transcriptText": "string",
      "unansweredQuestions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionItems` | array<string> | Suggested action items from the call. |
| `agentName` | string | Agent name. |
| `ai_success` | boolean | Whether AI post-processing succeeded. |
| `callDirection` | string | Call direction or source. |
| `callId` | string | Unique call ID. |
| `dashboardUrl` | string | Dashboard URL for the call. |
| `duration` | number | Call duration in minutes. |
| `endedReason` | string | Reason the call ended. |
| `followUp` | boolean | Whether follow-up is recommended. |
| `keyPoints` | array<string> | Key points extracted from the call. |
| `messages` | array<object> | Structured call message events. |
| `purpose` | string | Detected call purpose. |
| `recordingUrl` | string | Recording URL for the call. |
| `sentiment` | string | Overall call sentiment. |
| `summary` | string | AI-generated call summary. |
| `topic` | array<string> | Topics detected for the call. |
| `transcript` | array<object> | Structured transcript events. |
| `transcriptText` | string | Flattened transcript text. |
| `unansweredQuestions` | array<string> | Unanswered questions from the call. |

## Native endpoint

Through the native Phonely API, this operation is `POST /api/get-call` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call.md) for the provider-specific parameters and requirements.

