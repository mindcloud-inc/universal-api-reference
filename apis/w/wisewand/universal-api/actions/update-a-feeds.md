# Wisewand: Update a feeds

Updates an existing feed in your Wisewand workspace.

```
PUT https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/update-a-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/update-a-feeds" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "test-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/update-a-feeds', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "test-id"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native Wisewand API, this operation is `PATCH /v1/feeds/:id` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-feeds.md) for the provider-specific parameters and requirements.

