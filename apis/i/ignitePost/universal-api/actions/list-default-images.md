# IgnitePost: List Default Images

Retrieves available default images from IgnitePost.

```
GET https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/list-default-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgnitePost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/list-default-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ignitePost/latest/actions/list-default-images?${params}`, {
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
      "key": "string",
      "label": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string | IgnitePOST image key used in preview and order requests. |
| `label` | string | Display name of the stock image. |
| `url` | string | Hosted URL for the stock image asset. |

## Native endpoint

Through the native IgnitePost API, this operation is `GET /images` (base URL `https://dashboard.ignitepost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-default-images.md) for the provider-specific parameters and requirements.

