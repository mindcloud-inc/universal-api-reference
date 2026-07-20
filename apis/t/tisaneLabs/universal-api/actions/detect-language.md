# Tisane Labs: Detect Language

Detects input language in Tisane Labs.

```
GET https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/detect-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tisane Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/detect-language?connectionId=$CONNECTION_ID&content=c'est%20la%20vie" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content": "c'est la vie"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/detect-language?${params}`, {
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
| `content` | string | yes | Text fragment to analyze for language detection. Example: `c'est la vie`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languages` | string | no | Optional vertical-bar-delimited language codes to use as cues. Example: `es\|ar`. |
| `delimiter` | string | no | Optional regular expression for segmenting the fragment. Example: `[\r\n]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "languages": [
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
| `languages` | array<object> | Detected language spans with offsets, lengths, language codes, and scores. |

## Native endpoint

Through the native Tisane Labs API, this operation is `POST /detectLanguage` (base URL `https://api.tisane.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-language.md) for the provider-specific parameters and requirements.

