# XenForo: Delete Post

Deletes an existing post from XenForo.

```
DELETE https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/delete-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/delete-post?connectionId=$CONNECTION_ID&id=456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/delete-post?${params}`, {
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
| `id` | number | yes | ID of the post to delete. Example: `456`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hardDelete` | boolean | no | If true, permanently delete the post instead of soft deleting it. |
| `reason` | string | no | Reason shown for a soft deletion. Example: `Duplicate post`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the post was deleted. |

## Native endpoint

Through the native XenForo API, this operation is `DELETE /posts/:id/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post.md) for the provider-specific parameters and requirements.

