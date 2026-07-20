# Dev.to: Get Comment

Retrieves a Dev.to comment and its descendant comments by ID.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-comment?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-comment?${params}`, {
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
| `id` | string | yes | Comment ID code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body_html": "string",
      "children": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id_code": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body_html` | string |  |
| `children` | array<object> |  |
| `created_at` | date |  |
| `id_code` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Dev.to API, this operation is `GET /comments/:id` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

