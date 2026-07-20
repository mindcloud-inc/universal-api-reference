# Mihu AI: Get Full Transcript with Conversation Messages and Evaluations



```
GET https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-full-transcript-with-conversation-messages-and-evaluations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-full-transcript-with-conversation-messages-and-evaluations?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-full-transcript-with-conversation-messages-and-evaluations?${params}`, {
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
| `uuid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coachingAgentUuid": "string",
      "conversation": {
        "id": "string",
        "messages": [
          {
            "content": "string",
            "role": "string"
          }
        ],
        "plain": "string"
      },
      "evaluations": {},
      "id": "string",
      "processedAt": "2026-05-07T12:00:00.000Z",
      "qaAgentUuid": "string",
      "referenceId": "string",
      "session": {
        "id": "string",
        "status": "string",
        "type": "string"
      },
      "status": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coachingAgentUuid` | string |  |
| `conversation.id` | string |  |
| `conversation.messages[].content` | string |  |
| `conversation.messages[].role` | string |  |
| `conversation.plain` | string |  |
| `evaluations` | object |  |
| `id` | string |  |
| `processedAt` | date |  |
| `qaAgentUuid` | string |  |
| `referenceId` | string |  |
| `session.id` | string |  |
| `session.status` | string |  |
| `session.type` | string |  |
| `status` | string |  |
| `timestamp` | number |  |

## Native endpoint

Through the native Mihu AI API, this operation is `GET /api/v1/transcriptions/:uuid/transcript` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-transcript-with-conversation-messages-and-evaluations.md) for the provider-specific parameters and requirements.

