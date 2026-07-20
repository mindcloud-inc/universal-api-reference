# Vectara: Evaluate Factual Consistency

Evaluates generated text for factual consistency in Vectara.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/evaluate-factual-consistency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/evaluate-factual-consistency?connectionId=$CONNECTION_ID&generatedText=string&sourceTexts%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "generatedText": "string",
  "sourceTexts[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/evaluate-factual-consistency?${params}`, {
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
| `generatedText` | string | yes | Generated text to evaluate for factual consistency. |
| `sourceTexts[]` | array<string> | yes | Source passages used to verify the generated text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelParameters` | object | no | Optional model parameters for factual consistency evaluation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `score` | number | Predicted hallucination likelihood score. |

## Native endpoint

Through the native Vectara API, this operation is `POST /v2/evaluate_factual_consistency` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/evaluate-factual-consistency.md) for the provider-specific parameters and requirements.

