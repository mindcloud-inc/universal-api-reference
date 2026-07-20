# Wolfram Alpha: Get LLM Result with Geographic Context

Retrieves an LLM-ready Wolfram Alpha result with geographic context.

```
GET https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-llm-result-with-geographic-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wolfram Alpha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-llm-result-with-geographic-context?connectionId=$CONNECTION_ID&input=string&location=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string",
  "location": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/get-llm-result-with-geographic-context?${params}`, {
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
| `input` | string | yes |  |
| `location` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "query": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `query` | string | Original query text. |
| `result` | string | LLM-oriented answer text returned by Wolfram\|Alpha. |

## Native endpoint

Through the native Wolfram Alpha API, this operation is `GET https://www.wolframalpha.com/api/v1/llm-api` (base URL `https://api.wolframalpha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-llm-result-with-geographic-context.md) for the provider-specific parameters and requirements.

