# Tailwind: Delete Post

Deletes an existing post from Tailwind.

```
DELETE https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/delete-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tailwind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/delete-post?connectionId=$CONNECTION_ID&accountId=string&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/delete-post?${params}`, {
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
| `accountId` | string | yes | Pinterest account ID. |
| `postId` | string | yes | Tailwind post ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the post was deleted. |

## Native endpoint

Through the native Tailwind API, this operation is `DELETE /v1/accounts/:accountId/posts/:postId` (base URL `https://api-v1.tailwind.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post.md) for the provider-specific parameters and requirements.

