# SimpleLocalize: Auto-Translate Text

Creates an auto-translation job for text in SimpleLocalize.

```
POST https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/auto-translate-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/auto-translate-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetLanguage": "string",
  "translationProvider": "DEEPL",
  "sourceText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/auto-translate-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetLanguage": "string",
    "translationProvider": "DEEPL",
    "sourceText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetLanguage` | string | yes | Provider target language key |
| `targetProjectLanguage` | string | no | Project target language key (optional). It's required to load additional information about the target language (e.g. DeepL glossary). |
| `deeplFormality` | list | no | DeepL formality One of: `default, more, less`. |
| `description` | string | no | Description that will be used as a context for translation. It's useful for better translation quality. |
| `translationProvider` | list | yes | Provider for auto-translation One of: `DEEPL`, `GOOGLE_TRANSLATE`, `OPEN_AI`. |
| `sourceText` | string | yes | Source text to translate |
| `sourceProjectLanguage` | string | no | Project source language key (optional). It's required to load additional information about the source language (e.g. DeepL glossary). |
| `sourceLanguage` | string | no | Provider source language key (optional). If not provided, the source language will be detected automatically. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "translatedText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `translatedText` | string |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `POST /api/v1/auto-translate` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/auto-translate-text.md) for the provider-specific parameters and requirements.

