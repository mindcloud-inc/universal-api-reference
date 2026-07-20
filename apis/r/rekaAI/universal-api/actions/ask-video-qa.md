# Reka AI: Ask Video QA

Creates a video QA response in Reka AI.

```
POST https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/ask-video-qa
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/ask-video-qa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/ask-video-qa', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `video_id` | string | yes | Video identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "choices": [
        {}
      ],
      "id": "string",
      "model": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `choices` | array<object> | Answer choices. |
| `id` | string | Conversation identifier. |
| `model` | string | Model identifier. |
| `usage` | object | Usage summary. |

## Native endpoint

Through the native Reka AI API, this operation is `POST https://vision-agent.api.reka.ai/v1/qa/chat` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ask-video-qa.md) for the provider-specific parameters and requirements.

