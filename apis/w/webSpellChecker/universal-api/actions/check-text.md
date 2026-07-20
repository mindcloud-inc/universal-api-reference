# WebSpellChecker: Check Text

Checks text for spelling, grammar, and style issues in WebSpellChecker.

```
GET https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/check-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/check-text?connectionId=$CONNECTION_ID&text=Paste%20the%20text%20to%20check%20for%20spelling%20and%20grammar." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Paste the text to check for spelling and grammar."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/check-text?${params}`, {
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
| `text` | string | yes | The text to check. Example: `Paste the text to check for spelling and grammar.`. |
| `lang` | string | no | Language code to use for checking. Default: `en_US`. Example: `en_US`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `disableSpelling` | string | no | Disable spelling checks. Default: `false`. |
| `disableGrammar` | string | no | Disable grammar checks. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {
          "matches": [
            {
              "category": "string",
              "description": "string",
              "length": 1,
              "message": "string",
              "offset": 1,
              "probability": 1,
              "rule": "string",
              "suggestions": [
                "string"
              ],
              "type": "string"
            }
          ]
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
| `result` | array<object> | Top-level result entries returned by the check command. |
| `result[].matches` | array<object> | Detected spelling and grammar matches. |
| `result[].matches[].category` | string | Rule category. |
| `result[].matches[].description` | string | Rule description. |
| `result[].matches[].length` | number | Length of the matched text span. |
| `result[].matches[].message` | string | Provider message for the match. |
| `result[].matches[].offset` | number | Character offset of the match. |
| `result[].matches[].probability` | number | Provider confidence score. |
| `result[].matches[].rule` | string | Rule identifier. |
| `result[].matches[].suggestions` | array<string> | Suggested replacement values. |
| `result[].matches[].type` | string | Match type, such as spelling or grammar. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-text.md) for the provider-specific parameters and requirements.

