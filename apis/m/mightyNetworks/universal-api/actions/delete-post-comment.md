# Mighty Networks: Delete Post Comment

Deletes a comment from a post in Mighty Networks.

```
DELETE https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/delete-post-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/delete-post-comment?connectionId=$CONNECTION_ID&networkId=%7B%7Bcredentials.networkId%7D%7D&postId=123456789&id=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "networkId": "{{credentials.networkId}}",
  "postId": "123456789",
  "id": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/delete-post-comment?${params}`, {
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
| `networkId` | string | yes | The Mighty Networks network ID or subdomain for the request path. Default: `{{credentials.networkId}}`. |
| `postId` | number | yes | The ID of the post that owns the comment. Example: `123456789`. |
| `id` | number | yes | The ID of the comment to delete. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `DELETE /networks/:network_id/posts/:post_id/comments/:id` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post-comment.md) for the provider-specific parameters and requirements.

