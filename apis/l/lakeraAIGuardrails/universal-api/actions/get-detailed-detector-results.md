# Lakera AI Guardrails: Get Detailed Detector Results



```
GET https://connect.mindcloud.co/v1/universal/lakeraAIGuardrails/latest/actions/get-detailed-detector-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lakera AI Guardrails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lakeraAIGuardrails/latest/actions/get-detailed-detector-results?connectionId=$CONNECTION_ID&messages%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messages[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lakeraAIGuardrails/latest/actions/get-detailed-detector-results?${params}`, {
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
| `messages[]` | array<object> | yes | Messages comprising the LLM interaction history in OpenAI Chat Completions format. |
| `projectId` | string | no | Optional Lakera project ID. If omitted, Lakera uses the Guard default policy. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Optional request metadata such as user or session identifiers. |
| `devInfo` | boolean | no | Return Lakera Guard build information when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "requestUuid": "string"
      },
      "results": [
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
| `metadata` | object | Response metadata. |
| `metadata.requestUuid` | string | Unique Lakera request identifier. |
| `results` | array<object> | Detector confidence-level results. |

## Native endpoint

Through the native Lakera AI Guardrails API, this operation is `POST /guard/results` (base URL `https://api.lakera.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-detailed-detector-results.md) for the provider-specific parameters and requirements.

