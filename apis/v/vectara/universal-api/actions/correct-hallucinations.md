# Vectara: Correct Hallucinations

Corrects hallucinations in generated text with Vectara.

```
GET https://connect.mindcloud.co/v1/universal/vectara/latest/actions/correct-hallucinations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vectara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/correct-hallucinations?connectionId=$CONNECTION_ID&generatedText=string&documents%5B%5D=%5Bobject%20Object%5D&modelName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "generatedText": "string",
  "documents[]": "[object Object]",
  "modelName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/correct-hallucinations?${params}`, {
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
| `generatedText` | string | yes | Generated text to check and correct for hallucinations. |
| `documents[]` | array<object> | yes | Source document objects used for hallucination correction. |
| `modelName` | string | yes | Hallucination correction model name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no | Optional query context for correction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "corrected_text": "string",
      "corrections": [
        {}
      ],
      "model": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `corrected_text` | string | Corrected version of the input text. |
| `corrections` | array<object> | Corrections applied to the generated text. |
| `model` | string | Model used for hallucination correction. |

## Native endpoint

Through the native Vectara API, this operation is `POST /v2/hallucination_correctors/correct_hallucinations` (base URL `https://api.vectara.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/correct-hallucinations.md) for the provider-specific parameters and requirements.

