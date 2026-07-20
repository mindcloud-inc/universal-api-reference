# ProductLift: List Comments



```
GET https://connect.mindcloud.co/v1/universal/productLift/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductLift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productLift/latest/actions/list-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productLift/latest/actions/list-comments?${params}`, {
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
      "authorName": "Ava Chen",
      "content": "string",
      "createdAt": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorName` | string |  |
| `content` | string |  |
| `createdAt` | string |  |
| `id` | string |  |

## Native endpoint

Through the native ProductLift API, this operation is `GET /posts/{postId}/comments` (base URL `https://mindcloud.productlift.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

