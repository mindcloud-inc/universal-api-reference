# ClustDoc: List Templates By Language



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-templates-by-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-templates-by-language?connectionId=$CONNECTION_ID&language=pt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language": "pt"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-templates-by-language?${params}`, {
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
| `language` | string | yes | Template language code, for example pt. Default: `pt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": 1,
      "category": "string",
      "collect_phone": true,
      "color": "string",
      "created_at": "string",
      "deadline_type": "string",
      "id": 1,
      "is_live": true,
      "language": "string",
      "signature": "string",
      "team_id": 1,
      "title": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | number |  |
| `category` | string |  |
| `collect_phone` | boolean |  |
| `color` | string |  |
| `created_at` | string |  |
| `deadline_type` | string |  |
| `id` | number |  |
| `is_live` | boolean |  |
| `language` | string |  |
| `signature` | string |  |
| `team_id` | number |  |
| `title` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /templates` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates-by-language.md) for the provider-specific parameters and requirements.

