# Ghost: Delete Post

Deletes an existing post from Ghost.

```
DELETE https://connect.mindcloud.co/v1/universal/ghost/latest/actions/delete-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/delete-post?connectionId=$CONNECTION_ID&id=69b2eb8b8186310001a39584" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "69b2eb8b8186310001a39584"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ghost/latest/actions/delete-post?${params}`, {
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
| `id` | string | yes | Ghost post ID to delete. Example: `69b2eb8b8186310001a39584`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `DELETE /posts/:id/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post.md) for the provider-specific parameters and requirements.

