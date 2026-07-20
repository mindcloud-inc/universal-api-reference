# ContentStudio: Delete Post

Deletes a social media post from ContentStudio, optionally deleting it from platforms.

```
DELETE https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/delete-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/delete-post?connectionId=$CONNECTION_ID&post_id=string&workspace_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "post_id": "string",
  "workspace_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/delete-post?${params}`, {
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
| `account_ids[]` | array<string> | no | Specific platform account IDs to target. |
| `delete_from_social` | boolean | no | Delete from social platforms before removing from ContentStudio. |
| `post_id` | string | yes | ContentStudio post ID. |
| `workspace_id` | string | yes | ContentStudio workspace ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ContentStudio API returns.

## Native endpoint

Through the native ContentStudio API, this operation is `DELETE /workspaces/:workspace_id/posts/:post_id` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post.md) for the provider-specific parameters and requirements.

