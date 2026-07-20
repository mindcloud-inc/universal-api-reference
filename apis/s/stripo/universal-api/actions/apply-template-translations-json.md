# Stripo: Apply Template Translations JSON

Applies template translations from a JSON file in Stripo.

```
PUT https://connect.mindcloud.co/v1/universal/stripo/latest/actions/apply-template-translations-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/apply-template-translations-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "id": 1,
  "targetLanguages[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stripo/latest/actions/apply-template-translations-json', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "id": 1,
    "targetLanguages[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | JSON file containing translation data. |
| `id` | number | yes | The template ID. |
| `targetLanguages[]` | array<string> | yes | Target language codes in locale format. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Confirmation that template translation JSON was applied. |

## Native endpoint

Through the native Stripo API, this operation is `POST /templates/:id/translation-versions/json/apply` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-template-translations-json.md) for the provider-specific parameters and requirements.

