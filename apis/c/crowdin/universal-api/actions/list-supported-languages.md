# Crowdin: List Supported Languages

Retrieves supported languages from Crowdin.

```
GET https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-supported-languages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crowdin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-supported-languages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdin/latest/actions/list-supported-languages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "androidCode": "string",
      "dialectOf": "string",
      "editorCode": "string",
      "id": "string",
      "locale": "string",
      "name": "Ava Chen",
      "osxCode": "string",
      "osxLocale": "string",
      "pluralCategoryNames": [
        "Ava Chen"
      ],
      "pluralExamples": [
        "string"
      ],
      "pluralRules": "string",
      "textDirection": "string",
      "threeLettersCode": "string",
      "twoLettersCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `androidCode` | string |  |
| `dialectOf` | string |  |
| `editorCode` | string |  |
| `id` | string |  |
| `locale` | string |  |
| `name` | string |  |
| `osxCode` | string |  |
| `osxLocale` | string |  |
| `pluralCategoryNames` | array<string> |  |
| `pluralExamples` | array<string> |  |
| `pluralRules` | string |  |
| `textDirection` | string |  |
| `threeLettersCode` | string |  |
| `twoLettersCode` | string |  |

## Native endpoint

Through the native Crowdin API, this operation is `GET /languages` (base URL `https://api.crowdin.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-supported-languages.md) for the provider-specific parameters and requirements.

