# e-Gov: Search Tags

Finds tags in e-Gov by name.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/search-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/search-tags?connectionId=$CONNECTION_ID&limit=25&offset=0&query=%E4%BA%A4%E9%80%9A" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "交通"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/search-tags?${params}`, {
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
| `query` | string | yes | Default: `交通`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vocabulary_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "vocabulary_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `vocabulary_id` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /tag_search` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-tags.md) for the provider-specific parameters and requirements.

