# LinkupAPI: Generate Response

Generates an OpenAI-style response through LinkupAPI.

```
GET https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/generate-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkupAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/generate-response?connectionId=$CONNECTION_ID&input=string&model=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string",
  "model": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/generate-response?${params}`, {
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
| `input` | string | yes | The prompt or input to generate a response for. |
| `model` | string | yes | The Linkup model to use for response generation. One of: `0`, `1`. |
| `instructions` | string | no | Optional system-style instructions for the response. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | object | no | Optional text-format configuration object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "error": {},
      "id": "string",
      "model": "string",
      "object": "string",
      "output_text": "string",
      "output": [
        [
          {}
        ]
      ],
      "parallel_tool_calls": true,
      "tool_choice": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number | The Unix timestamp when the response was created. |
| `error` | object | The error payload when generation fails. |
| `id` | string | The Linkup response ID. |
| `model` | string | The Linkup model used to generate the response. |
| `object` | string | The response object type. |
| `output_text` | string | The generated response text. |
| `output[]` | array<object> | The structured output items returned by Linkup. |
| `parallel_tool_calls` | boolean | Whether Linkup executed parallel tool calls. |
| `tool_choice` | string | The tool-selection mode used by Linkup. |

## Native endpoint

Through the native LinkupAPI API, this operation is `POST /responses` (base URL `https://api.linkup.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-response.md) for the provider-specific parameters and requirements.

