# Placedog: List Images

Retrieves available Placedog image IDs and attribution details.

```
GET https://connect.mindcloud.co/v1/universal/placedog/latest/actions/list-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placedog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placedog/latest/actions/list-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placedog/latest/actions/list-images?${params}`, {
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
      "attributionName": "Ava Chen",
      "attributionUrl": "https://example.com",
      "id": 1,
      "placeholderUrl": "https://example.com",
      "sampleImageUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributionName` | string |  |
| `attributionUrl` | string |  |
| `id` | number |  |
| `placeholderUrl` | string |  |
| `sampleImageUrl` | string |  |

## Native endpoint

Through the native Placedog API, this operation is `GET /images` (base URL `https://placedog.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-images.md) for the provider-specific parameters and requirements.

