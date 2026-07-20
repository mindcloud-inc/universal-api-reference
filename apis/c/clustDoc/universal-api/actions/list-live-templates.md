# ClustDoc: List Live Templates



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-live-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-live-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-live-templates?${params}`, {
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

Through the native ClustDoc API, this operation is `GET /templates` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-live-templates.md) for the provider-specific parameters and requirements.

