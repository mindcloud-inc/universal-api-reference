# Wikibot: Anonymize Text

Anonymizes text in Wikibot.

```
POST https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/anonymize-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikibot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/anonymize-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "Customer Ivan Petrov called from +7 999 123-45-67."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/anonymize-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "Customer Ivan Petrov called from +7 999 123-45-67."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Source text to anonymize. Example: `Customer Ivan Petrov called from +7 999 123-45-67.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `existingReplacements[]` | array<object> | no | Existing replacement map entries to apply or account for during anonymization. Accepts multiple values as an array. |
| `ignoredNames` | string | no | Optional names to ignore during anonymization. Example: `Ivan, Maria`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anonymized_text": "string",
      "replacements": [
        {
          "entity_type": "string",
          "fake": "string",
          "ignored_names": "Ava Chen",
          "original": "string"
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
| `anonymized_text` | string | Text with PII replaced. |
| `replacements` | array<object> | Replacement map entries produced by anonymization. |
| `replacements[].entity_type` | string | PII entity type. |
| `replacements[].fake` | string | Replacement value. |
| `replacements[].ignored_names` | string | Ignored names associated with the replacement. |
| `replacements[].original` | string | Original value. |

## Native endpoint

Through the native Wikibot API, this operation is `POST /bot/anonymize` (base URL `https://api.wikibot.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/anonymize-text.md) for the provider-specific parameters and requirements.

