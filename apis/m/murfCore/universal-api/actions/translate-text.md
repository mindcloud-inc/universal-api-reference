# Murf Core: Translate Text

Translates text into another language with Murf Core.

```
POST https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/translate-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Murf Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/translate-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetLanguage": "string",
  "texts[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/murfCore/latest/actions/translate-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetLanguage": "string",
    "texts[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetLanguage` | string | yes | Language code for the translated output. |
| `texts[]` | array<string> | yes | List of source texts to translate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "translations": [
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
| `metadata` | object | Translation metadata including target language, character counts, and credits used. |
| `translations` | array<object> | Translated text rows paired with their source text. |

## Native endpoint

Through the native Murf Core API, this operation is `POST /v1/text/translate` (base URL `https://api.murf.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-text.md) for the provider-specific parameters and requirements.

