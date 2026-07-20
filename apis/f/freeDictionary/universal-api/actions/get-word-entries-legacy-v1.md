# Free Dictionary: Get Word Entries (Legacy v1)



```
GET https://connect.mindcloud.co/v1/universal/freeDictionary/latest/actions/get-word-entries-legacy-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Free Dictionary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeDictionary/latest/actions/get-word-entries-legacy-v1?connectionId=$CONNECTION_ID&language=string&word=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language": "string",
  "word": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freeDictionary/latest/actions/get-word-entries-legacy-v1?${params}`, {
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
| `language` | string | yes | Supported language code for the dictionary lookup. Upstream source supports hi, en, en_GB, en_US, es, fr, ja, cs, nl, sk, ru, de, it, ko, pt-BR, ar, and tr. |
| `word` | string | yes | The English word to look up. |
| `include` | string | no | Optional comma-separated expansions. Use `example` to include full examples arrays in the response where available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "license": {},
      "meaning": {},
      "phonetics": [
        {}
      ],
      "sourceUrls": [
        "https://example.com"
      ],
      "word": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `license` | object | License metadata for the dictionary content when provided. |
| `meaning` | object | Definitions grouped by part of speech under the legacy v1 response contract. |
| `phonetics` | array<object> | Pronunciation variants, audio links, and licensing details. |
| `sourceUrls` | array<string> | Source dictionary pages for the returned entries. |
| `word` | string | The requested English word. |

## Native endpoint

Through the native Free Dictionary API, this operation is `GET /api/v1/entries/:language/:word` (base URL `https://api.dictionaryapi.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-word-entries-legacy-v1.md) for the provider-specific parameters and requirements.

