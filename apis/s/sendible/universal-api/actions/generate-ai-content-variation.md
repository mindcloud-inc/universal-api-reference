# Sendible: Generate AI Content Variation



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/generate-ai-content-variation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/generate-ai-content-variation?connectionId=$CONNECTION_ID&option=string&prompt=string&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "option": "string",
  "prompt": "string",
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/generate-ai-content-variation?${params}`, {
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
| `option` | string | yes | Transformation option such as rephrase. |
| `prompt` | string | yes | Prompt text to transform or rephrase. |
| `sessionId` | string | yes | AI session identifier. |
| `socialNetwork` | string | no | Optional social network when rephrasing for a specific channel. |
| `targetAudience` | string | no | Optional audience hint. |
| `tone` | string | no | Optional tone hint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> |  |

## Native endpoint

Through the native Sendible API, this operation is `GET 1.0/api/ai/content` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-ai-content-variation.md) for the provider-specific parameters and requirements.

