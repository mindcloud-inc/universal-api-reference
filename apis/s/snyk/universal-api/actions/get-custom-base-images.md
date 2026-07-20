# Snyk: List Custom Base Images

Retrieves custom base images from Snyk.

```
GET https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-custom-base-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snyk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-custom-base-images?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-custom-base-images?${params}`, {
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
      "data": [
        {}
      ],
      "jsonapi": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Custom base images returned by Snyk. |
| `jsonapi` | object | JSON:API metadata. |
| `links` | object | Pagination and self links. |

## Native endpoint

Through the native Snyk API, this operation is `GET /custom_base_images` (base URL `https://api.snyk.io/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-custom-base-images.md) for the provider-specific parameters and requirements.

