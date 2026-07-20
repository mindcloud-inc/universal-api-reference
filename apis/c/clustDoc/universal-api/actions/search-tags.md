# ClustDoc: Search Tags



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-tags?connectionId=$CONNECTION_ID&search=test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search": "test"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-tags?${params}`, {
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
| `search` | string | yes | Search text for tags. Default: `test`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created_at": "string",
      "id": 1,
      "name": "Ava Chen",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created_at` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /tags` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tags.md) for the provider-specific parameters and requirements.

