# ActivityInfo: Get Database Translations

Retrieves ActivityInfo translations by dictionary and language.

```
GET https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-translations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActivityInfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-translations?connectionId=$CONNECTION_ID&databaseId=string&dictionaryId=string&language=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "databaseId": "string",
  "dictionaryId": "string",
  "language": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/get-database-translations?${params}`, {
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
| `databaseId` | string | yes | ActivityInfo database ID. |
| `dictionaryId` | string | yes | Dictionary ID, such as database or form/{formId}. |
| `language` | string | yes | ISO two-letter language code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "databaseId": "string",
      "dictionaryId": "string",
      "id": {},
      "language": "string",
      "translatedStrings": [
        {}
      ],
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `databaseId` | string | Database ID. |
| `dictionaryId` | string | Dictionary ID. |
| `id` | object | Dictionary ID object. |
| `language` | string | Language code. |
| `translatedStrings` | array<object> | Translated strings. |
| `version` | number | Dictionary version. |

## Native endpoint

Through the native ActivityInfo API, this operation is `GET /resources/databases/:databaseId/dictionary/:dictionaryId/:language` (base URL `https://www.activityinfo.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-database-translations.md) for the provider-specific parameters and requirements.

