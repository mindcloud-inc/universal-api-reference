# SimpleLocalize: Export Translations

Exports translations from SimpleLocalize as files.

```
GET https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/export-translations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/export-translations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/export-translations?${params}`, {
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
| `downloadFormat` | list | no | One of: `android`, `android-strings`, `android-xml`, `csv-translations`, `excel`, `java-properties`, `javascript`, `localizable-strings`, `localizable-strings-dict`, `localizable-xcstrings`, `module-exports`, `multi-language-json`, `php-array`, `po-pot`, `qt-linguist`, `resx`, `simplelocalize-json`, `single-language-json`, `string-resources`, `tsv`, `yaml`. |
| `downloadOptions[]` | array<string> | no |  |
| `languageKeys[]` | array<string> | no |  |
| `tags[]` | array<string> | no |  |
| `languageOrder[]` | array<string> | no |  |
| `customerId` | string | no |  |
| `sort` | list | no | One of: `DEFAULT`, `IMPORT_ORDER`, `NAMESPACES`, `NEWEST_KEYS_FIRST`, `NEWEST_KEYS_LAST`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "files": [
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
| `files` | array<object> |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `GET /api/v4/export` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-translations.md) for the provider-specific parameters and requirements.

