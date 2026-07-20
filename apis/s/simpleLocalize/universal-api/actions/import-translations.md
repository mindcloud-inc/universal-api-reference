# SimpleLocalize: Import Translations

Imports translations from a file into SimpleLocalize.

```
POST https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/import-translations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/import-translations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uploadFormat": "android"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/import-translations', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uploadFormat": "android"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uploadFormat` | list | yes | One of: `android`, `android-strings`, `android-xml`, `csv-translations`, `excel`, `java-properties`, `javascript`, `localizable-strings`, `localizable-strings-dict`, `localizable-xcstrings`, `module-exports`, `multi-language-json`, `php-array`, `po-pot`, `qt-linguist`, `resx`, `simplelocalize-json`, `single-language-json`, `string-resources`, `tsv`, `yaml`. |
| `importOptions[]` | array<string> | no |  |
| `languageKey` | string | no |  |
| `customerId` | string | no |  |
| `namespace` | string | no |  |
| `tags[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "foundLanguages": [
        {}
      ],
      "numberOfKeysFound": 1,
      "numberOfUniqueKeysFound": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `foundLanguages` | array<object> |  |
| `numberOfKeysFound` | number |  |
| `numberOfUniqueKeysFound` | number |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `POST /api/v2/import` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-translations.md) for the provider-specific parameters and requirements.

