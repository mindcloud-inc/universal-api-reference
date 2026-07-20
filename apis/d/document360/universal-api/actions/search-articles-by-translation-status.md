# Document360: Search Articles by Translation Status



```
GET https://connect.mindcloud.co/v1/universal/document360/latest/actions/search-articles-by-translation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/search-articles-by-translation-status?connectionId=$CONNECTION_ID&projectVersionId=string&langCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectVersionId": "string",
  "langCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/search-articles-by-translation-status?${params}`, {
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
| `projectVersionId` | string | yes | The ID of the version |
| `langCode` | string | yes | The language code of the version |
| `status` | number | no | Translation status filter |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryId": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Document360 API, this operation is `GET /v2/Translations/:projectVersionId/:langCode` (base URL `https://apihub.document360.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-articles-by-translation-status.md) for the provider-specific parameters and requirements.

