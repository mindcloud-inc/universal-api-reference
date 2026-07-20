# GPT Chatbot: List Sessions

Retrieves sessions for a chatbot in GPT Chatbot.

```
GET https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPT Chatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-sessions?connectionId=$CONNECTION_ID&chatbotUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatbotUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTChatbot/latest/actions/list-sessions?${params}`, {
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
| `chatbotUuid` | string | yes | Chatbot uuid. |
| `endTimestamp` | date | no | Filter sessions created before this timestamp (inclusive), in ISO 8601 UTC. |
| `startTimestamp` | date | no | Filter sessions created after this timestamp (inclusive), in ISO 8601 UTC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "ipAddress": "string",
      "meta": {},
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `ipAddress` | string |  |
| `meta` | object |  |
| `modifiedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native GPT Chatbot API, this operation is `GET /chatbot/:uuid/sessions` (base URL `https://app.gptchatbot.it/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

