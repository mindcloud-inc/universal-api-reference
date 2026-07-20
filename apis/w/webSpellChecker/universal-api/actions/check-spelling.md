# WebSpellChecker: Check Spelling

Checks text for spelling errors in WebSpellChecker.

```
GET https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/check-spelling
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/check-spelling?connectionId=$CONNECTION_ID&text=Paste%20the%20text%20to%20spell-check." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Paste the text to spell-check."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/check-spelling?${params}`, {
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
| `text` | string | yes | The text to spell-check. Example: `Paste the text to spell-check.`. |
| `slang` | string | no | Language code to use for spelling. Default: `en_US`. Example: `en_US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "suggestions": [
            "string"
          ],
          "ud": true,
          "url": true,
          "word": "string"
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
| `items` | array<object> | Misspelled words returned by the spelling check. |
| `items[].suggestions` | array<string> | Suggested spellings. |
| `items[].ud` | boolean | Whether the word comes from a user dictionary. |
| `items[].url` | boolean | Whether the token is recognized as a URL. |
| `items[].word` | string | Original misspelled word. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-spelling.md) for the provider-specific parameters and requirements.

