# Maildrip: Generate email subject or body content using AI



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/generate-email-subject-or-body-content-using-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/generate-email-subject-or-body-content-using-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "prompt": "string",
  "audience": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/generate-email-subject-or-body-content-using-ai', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "prompt": "string",
    "audience": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Type of content to generate (subject or body) |
| `prompt` | string | yes | The prompt or context for the AI to use |
| `audience` | string | yes | The target audience for the email |
| `sender` | string | no | The sender persona for the email |
| `goal` | string | no | The goal of the email |
| `tone` | string | no | The tone of the email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | The generated subject or body content |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/ai-assistant/generate` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-email-subject-or-body-content-using-ai.md) for the provider-specific parameters and requirements.

