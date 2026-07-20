# Wisewand: Get a updateposts

Retrieves an update post from your Wisewand workspace.

```
GET https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-a-updateposts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-a-updateposts?connectionId=$CONNECTION_ID&id=test-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "test-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-a-updateposts?${params}`, {
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
| `id` | string | yes | Wisewand path parameter `id`. Default: `test-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cover_image": "string",
      "created_at": "string",
      "data": {},
      "id": "string",
      "is_published": true,
      "last_output_id": "string",
      "maker_id": "string",
      "name": "Ava Chen",
      "project_id": "string",
      "status": "string",
      "status_detail": "string",
      "title": "string",
      "updated_at": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cover_image` | string |  |
| `created_at` | string |  |
| `data` | object |  |
| `id` | string |  |
| `is_published` | boolean |  |
| `last_output_id` | string |  |
| `maker_id` | string |  |
| `name` | string |  |
| `project_id` | string |  |
| `status` | string |  |
| `status_detail` | string |  |
| `title` | string |  |
| `updated_at` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Wisewand API, this operation is `GET /v1/updateposts/:id` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-updateposts.md) for the provider-specific parameters and requirements.

