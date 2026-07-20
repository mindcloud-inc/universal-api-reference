# Open AI: Count Response Input Tokens

Counts response input tokens in Open AI.

```
GET https://connect.mindcloud.co/v1/universal/openAi/latest/actions/count-response-input-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/count-response-input-tokens?connectionId=$CONNECTION_ID&input=Tell%20me%20a%20short%20joke.&model=gpt-4.1-mini" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "Tell me a short joke.",
  "model": "gpt-4.1-mini"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openAi/latest/actions/count-response-input-tokens?${params}`, {
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
| `input` | string | yes | Input content to count tokens for. Default: `Tell me a short joke.`. |
| `model` | string | yes | Model ID used to count input tokens. Default: `gpt-4.1-mini`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input_tokens": 1,
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input_tokens` | number | Counted input tokens. |
| `object` | string | Response type. |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/responses/input_tokens` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-response-input-tokens.md) for the provider-specific parameters and requirements.

