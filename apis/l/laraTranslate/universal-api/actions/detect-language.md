# Lara Translate: Detect language

Detects the source language of text in Lara Translate.

```
GET https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/detect-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lara Translate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/detect-language?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/detect-language?${params}`, {
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
| `text` | string | yes | Text to detect language for. |
| `hint` | string | no | Optional language hint to guide detection. Example: `en`. |
| `passlist[]` | array<string> | no | Optional list of allowed language codes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "language": "string",
      "predictions": [
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
| `contentType` | string | Detected content type. |
| `language` | string | Detected language code. |
| `predictions` | array<object> | Candidate language predictions with confidence. |

## Native endpoint

Through the native Lara Translate API, this operation is `POST /` (base URL `https://mcp-v2.laratranslate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-language.md) for the provider-specific parameters and requirements.

