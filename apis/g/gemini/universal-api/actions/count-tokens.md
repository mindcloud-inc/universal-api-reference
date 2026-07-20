# Gemini: Count Tokens

Counts tokens for content in Gemini.

```
GET https://connect.mindcloud.co/v1/universal/gemini/latest/actions/count-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/count-tokens?connectionId=$CONNECTION_ID&model=gemini-2.5-flash%3AcountTokens" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "model": "gemini-2.5-flash:countTokens"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gemini/latest/actions/count-tokens?${params}`, {
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
| `model` | string | yes | Required. Model endpoint token including suffix, for example gemini-2.5-flash:countTokens. Example: `gemini-2.5-flash:countTokens`. |
| `contents[]` | array<object> | no | Optional prompt contents to tokenize. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `generateContentRequest` | object | no | Optional full GenerateContentRequest payload (mutually exclusive with contents). Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "promptTokensDetails": [
        {}
      ],
      "totalTokens": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `promptTokensDetails` | array<object> | Token details by modality. |
| `totalTokens` | number | Total token count for the supplied input. |

## Native endpoint

Through the native Gemini API, this operation is `POST v1beta/models/:model` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-tokens.md) for the provider-specific parameters and requirements.

