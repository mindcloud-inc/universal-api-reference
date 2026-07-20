# Google AI Studio: Get Model

Retrieves a Gemini model from Google AI Studio.

```
GET https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google AI Studio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/get-model?connectionId=$CONNECTION_ID&model=gemini-2.5-flash" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "model": "gemini-2.5-flash"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAIStudio/latest/actions/get-model?${params}`, {
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
| `model` | string | yes | Required. Use the bare model ID (no `models/` prefix), for example `gemini-2.5-pro`. Example: `gemini-2.5-flash`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "displayName": "Ava Chen",
      "inputTokenLimit": 1,
      "name": "Ava Chen",
      "outputTokenLimit": 1,
      "supportedGenerationMethods": [
        "string"
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Provider model description. |
| `displayName` | string | Human-friendly model name. |
| `inputTokenLimit` | number | Maximum input token count. |
| `name` | string | Model resource name. |
| `outputTokenLimit` | number | Maximum output token count. |
| `supportedGenerationMethods` | array<string> | Supported methods for this model. |
| `version` | string | Model version string. |

## Native endpoint

Through the native Google AI Studio API, this operation is `GET v1beta/models/:model` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

