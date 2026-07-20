# WebSpellChecker: Detect Language

Finds likely languages for text in WebSpellChecker.

```
GET https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/detect-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/detect-language?connectionId=$CONNECTION_ID&text=Paste%20the%20text%20whose%20language%20you%20want%20to%20detect." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Paste the text whose language you want to detect."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/detect-language?${params}`, {
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
| `text` | string | yes | The text to analyze for language detection. Example: `Paste the text whose language you want to detect.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "LangName": "Ava Chen",
          "LangShortCode": "string",
          "Proportion": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Detected language candidates. |
| `items[].LangName` | string | Detected language display name. |
| `items[].LangShortCode` | string | Detected language code. |
| `items[].Proportion` | number | Confidence proportion for the detected language. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-language.md) for the provider-specific parameters and requirements.

