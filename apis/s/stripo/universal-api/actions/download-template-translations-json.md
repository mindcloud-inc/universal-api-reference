# Stripo: Download Template Translations JSON

Downloads template translations as a JSON file from Stripo.

```
GET https://connect.mindcloud.co/v1/universal/stripo/latest/actions/download-template-translations-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stripo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stripo/latest/actions/download-template-translations-json?connectionId=$CONNECTION_ID&id=1&targetLanguages%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "targetLanguages[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stripo/latest/actions/download-template-translations-json?${params}`, {
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
| `id` | number | yes | The template ID. |
| `targetLanguages[]` | array<string> | yes | Target language codes in locale format. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "targetLanguages": [
        "string"
      ],
      "translations": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `targetLanguages` | array<string> | Target language codes included in the translation JSON request. |
| `translations` | object | Translation JSON payload returned by Stripo. |

## Native endpoint

Through the native Stripo API, this operation is `POST /templates/:id/translation-versions/json` (base URL `https://my.stripo.email/emailgeneration/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-template-translations-json.md) for the provider-specific parameters and requirements.

