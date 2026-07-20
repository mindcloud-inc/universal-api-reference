# Wisewand: Get a feeds

Retrieves a feed from your Wisewand workspace.

```
GET https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-a-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-a-feeds?connectionId=$CONNECTION_ID&id=test-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "test-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-a-feeds?${params}`, {
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
      "color": "string",
      "config": "string",
      "created_at": "string",
      "enable_generation": true,
      "entity_type": "string",
      "error": "string",
      "filtering_brief": "string",
      "frequency": "string",
      "icon": "string",
      "id": "string",
      "is_active": true,
      "last_fetched_at": "string",
      "limit": 1,
      "project_id": "string",
      "sort_by": "string",
      "title": "string",
      "url": "https://example.com",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `config` | string |  |
| `created_at` | string |  |
| `enable_generation` | boolean |  |
| `entity_type` | string |  |
| `error` | string |  |
| `filtering_brief` | string |  |
| `frequency` | string |  |
| `icon` | string |  |
| `id` | string |  |
| `is_active` | boolean |  |
| `last_fetched_at` | string |  |
| `limit` | number |  |
| `project_id` | string |  |
| `sort_by` | string |  |
| `title` | string |  |
| `url` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Wisewand API, this operation is `GET /v1/feeds/:id` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-feeds.md) for the provider-specific parameters and requirements.

