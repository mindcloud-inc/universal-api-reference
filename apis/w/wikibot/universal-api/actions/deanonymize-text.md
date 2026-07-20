# Wikibot: Deanonymize Text

Deanonymizes text in Wikibot.

```
POST https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/deanonymize-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wikibot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/deanonymize-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "anonymizedText": "Customer PERSON_1 called from PHONE_NUMBER_1.",
  "replacements[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wikibot/latest/actions/deanonymize-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "anonymizedText": "Customer PERSON_1 called from PHONE_NUMBER_1.",
    "replacements[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `anonymizedText` | string | yes | Anonymized text that contains replacement fake values. Example: `Customer PERSON_1 called from PHONE_NUMBER_1.`. |
| `replacements[]` | array<object> | yes | Replacement map entries with fake and original values. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deanonymized_text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deanonymized_text` | string | Deanonymized text with original values restored. |

## Native endpoint

Through the native Wikibot API, this operation is `POST /bot/deanonymize` (base URL `https://api.wikibot.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deanonymize-text.md) for the provider-specific parameters and requirements.

