# Rosette Text Analytics: Translate Name



```
GET https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/translate-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rosette Text Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/translate-name?connectionId=$CONNECTION_ID&name=Ava%20Chen&targetLanguage=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "targetLanguage": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/translate-name?${params}`, {
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
| `name` | string | yes | Name to transliterate. |
| `targetLanguage` | string | yes | Three-letter ISO 639-3 target language code. |
| `sourceScript` | string | no | Script of the input name as a four-letter ISO 15924 code. |
| `sourceLanguageOfUse` | string | no | Language of the name as used in the input, as a three-letter ISO 639-3 code. |
| `sourceLanguageOfOrigin` | string | no | Native language the name originates in, as a three-letter ISO 639-3 code. |
| `targetScript` | string | no | Four-letter ISO 15924 target script code. |
| `entityType` | string | no | PERSON (default), LOCATION, or ORGANIZATION. Default: `PERSON`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetScheme` | string | no | Advanced transliteration scheme abbreviation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidence": 1,
      "extendedInformation": {},
      "sourceLanguageOfUse": "string",
      "sourceScript": "string",
      "targetLanguage": "string",
      "targetScheme": "string",
      "targetScript": "string",
      "translation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | number |  |
| `extendedInformation` | object |  |
| `sourceLanguageOfUse` | string |  |
| `sourceScript` | string |  |
| `targetLanguage` | string |  |
| `targetScheme` | string |  |
| `targetScript` | string |  |
| `translation` | string |  |

## Native endpoint

Through the native Rosette Text Analytics API, this operation is `POST /name-translation` (base URL `https://api.rosette.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-name.md) for the provider-specific parameters and requirements.

