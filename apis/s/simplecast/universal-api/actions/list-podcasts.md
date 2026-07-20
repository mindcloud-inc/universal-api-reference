# Simplecast: List Podcasts

Retrieves podcasts from Simplecast.

```
GET https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcasts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplecast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcasts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcasts?${params}`, {
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
      "collection": [
        {}
      ],
      "count": 1,
      "data": {},
      "description": "string",
      "href": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "title": "string",
      "total": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> | Returned collection items. |
| `count` | number | Returned item count. |
| `data` | object | Response data object. |
| `description` | string | Resource description. |
| `href` | string | Simplecast API URL for the resource. |
| `id` | string | Resource identifier. |
| `name` | string | Display name. |
| `status` | string | Resource status. |
| `title` | string | Display title. |
| `total` | number | Total available item count. |
| `url` | string | Related URL. |

## Native endpoint

Through the native Simplecast API, this operation is `GET /podcasts` (base URL `https://api.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-podcasts.md) for the provider-specific parameters and requirements.

