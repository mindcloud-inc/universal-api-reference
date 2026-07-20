# Flotiq: List Media Objects

Retrieves media objects from your Flotiq project.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/list-media-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/list-media-objects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/list-media-objects?${params}`, {
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
      "alt": "string",
      "extension": "string",
      "externalId": "string",
      "fileName": "Ava Chen",
      "height": 1,
      "id": "string",
      "internal": {},
      "mimeType": "string",
      "size": 1,
      "source": "string",
      "tags": [
        {}
      ],
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "variants": [
        {}
      ],
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt` | string |  |
| `extension` | string |  |
| `externalId` | string |  |
| `fileName` | string |  |
| `height` | number |  |
| `id` | string |  |
| `internal` | object |  |
| `mimeType` | string |  |
| `size` | number |  |
| `source` | string |  |
| `tags` | array<object> |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `variants` | array<object> |  |
| `width` | number |  |

## Native endpoint

Through the native Flotiq API, this operation is `GET /content/_media` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-media-objects.md) for the provider-specific parameters and requirements.

