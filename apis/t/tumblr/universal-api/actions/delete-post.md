# Tumblr: Delete Post

Deletes an existing post from Tumblr.

```
DELETE https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/delete-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/delete-post?connectionId=$CONNECTION_ID&blogIdentifier=mindcloudapps&postId=1772822948" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blogIdentifier": "mindcloudapps",
  "postId": "1772822948"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/delete-post?${params}`, {
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
| `blogIdentifier` | string | yes | Any Tumblr blog identifier for the target blog. Example: `mindcloudapps`. |
| `postId` | string | yes | ID of the post to delete. Example: `1772822948`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "idString": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `idString` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `POST /v2/blog/:blogIdentifier/post/delete` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post.md) for the provider-specific parameters and requirements.

