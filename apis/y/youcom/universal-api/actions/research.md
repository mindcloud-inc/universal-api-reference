# You.com: Research

Retrieves a research report from You.com.

```
GET https://connect.mindcloud.co/v1/universal/youcom/latest/actions/research
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a You.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youcom/latest/actions/research?connectionId=$CONNECTION_ID&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youcom/latest/actions/research?${params}`, {
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
| `input` | string | yes | Research question or complex query. |
| `researchEffort` | string | no | How deeply the API should research. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "output": {
        "content": "string",
        "contentType": "string",
        "sources": [
          [
            {}
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `output` | object | Top-level research response. |
| `output.content` | string | Synthesized research answer content. |
| `output.contentType` | string | Content type returned for the research answer. |
| `output.sources[]` | array<object> | Supporting sources used by the research answer. |
| `output.sources[].snippets[]` | array<string> | Supporting source snippets. |
| `output.sources[].title` | string | Source title. |
| `output.sources[].url` | string | Source URL. |

## Native endpoint

Through the native You.com API, this operation is `POST /v1/research` (base URL `https://api.you.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/research.md) for the provider-specific parameters and requirements.

