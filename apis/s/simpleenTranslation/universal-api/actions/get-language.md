# Simpleen Translation: Get Language

Retrieves a language from Simpleen Translation.

```
GET https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/get-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpleen Translation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/get-language?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/get-language?${params}`, {
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
| `id` | number | yes | ID of the language to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isRtl": true,
      "language": "string",
      "name": "Ava Chen",
      "onlySource": true,
      "source": true,
      "target": true,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | number |  |
| `isRtl` | boolean |  |
| `language` | string |  |
| `name` | string |  |
| `onlySource` | boolean |  |
| `source` | boolean |  |
| `target` | boolean |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Simpleen Translation API, this operation is `GET /languages/:id` (base URL `https://api.simpleen.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-language.md) for the provider-specific parameters and requirements.

