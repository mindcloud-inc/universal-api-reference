# Hy.page: Archive Post



```
DELETE https://connect.mindcloud.co/v1/universal/hypage/latest/actions/archive-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/archive-post?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hypage/latest/actions/archive-post?${params}`, {
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
| `id` | string | yes | Post ID to archive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Hy.page API, this operation is `DELETE /hyax-api/v1/posts/:id` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-post.md) for the provider-specific parameters and requirements.

