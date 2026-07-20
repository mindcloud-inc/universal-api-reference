# Late: Delete Post



```
DELETE https://connect.mindcloud.co/v1/universal/late/latest/actions/delete-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/late/latest/actions/delete-post?connectionId=$CONNECTION_ID&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/late/latest/actions/delete-post?${params}`, {
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
| `postId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider success message. |

## Native endpoint

Through the native Late API, this operation is `DELETE /posts/:postId` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post.md) for the provider-specific parameters and requirements.

