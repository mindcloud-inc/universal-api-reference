# WebSpellChecker: Grammar Check

Checks text for grammar issues in WebSpellChecker.

```
GET https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/grammar-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebSpellChecker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/grammar-check?connectionId=$CONNECTION_ID&text=Paste%20the%20text%20to%20grammar-check." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Paste the text to grammar-check."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webSpellChecker/latest/actions/grammar-check?${params}`, {
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
| `slang` | string | no | Language code to use for grammar checks. Default: `en_US`. Example: `en_US`. |
| `text` | string | yes | The text to grammar-check. Example: `Paste the text to grammar-check.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "matches": [
            {
              "length": 1,
              "message": "string",
              "offset": 1,
              "rule": {
                "category": "string",
                "id": "string"
              },
              "suggestions": [
                "string"
              ]
            }
          ],
          "sentence": "string"
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
| `items` | array<object> | Sentences returned by the grammar check. |
| `items[].matches` | array<object> | Detected grammar matches for the sentence. |
| `items[].matches[].length` | number | Length of the matched text span. |
| `items[].matches[].message` | string | Provider message for the grammar finding. |
| `items[].matches[].offset` | number | Character offset of the finding. |
| `items[].matches[].rule` | object | Rule metadata. |
| `items[].matches[].rule.category` | string | Rule category. |
| `items[].matches[].rule.id` | string | Rule identifier. |
| `items[].matches[].suggestions` | array<string> | Suggested corrections. |
| `items[].sentence` | string | Sentence text that was analyzed. |

## Native endpoint

Through the native WebSpellChecker API, this operation is `GET /` (base URL `https://svc.webspellchecker.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/grammar-check.md) for the provider-specific parameters and requirements.

