# Wisewand: Update projects

Updates an existing project in your Wisewand workspace.

```
PUT https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/update-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/update-projects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "test-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/update-projects', {
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
      "author": 1,
      "brief": "string",
      "brief_config": {},
      "category": 1,
      "color": "string",
      "connection": "string",
      "created_at": "string",
      "feeds_config": {},
      "feeds_count": 1,
      "id": "string",
      "is_brief_config_active": true,
      "is_quota_active": true,
      "persona": "string",
      "quota_limit": 1,
      "quota_period": "string",
      "quota_value": 1,
      "title": "string",
      "updated_at": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | number |  |
| `brief` | string |  |
| `brief_config` | object |  |
| `category` | number |  |
| `color` | string |  |
| `connection` | string |  |
| `created_at` | string |  |
| `feeds_config` | object |  |
| `feeds_count` | number | The number of feeds in the project. |
| `id` | string |  |
| `is_brief_config_active` | boolean | Whether the brief config is active. |
| `is_quota_active` | boolean |  |
| `persona` | string |  |
| `quota_limit` | number |  |
| `quota_period` | string |  |
| `quota_value` | number |  |
| `title` | string |  |
| `updated_at` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Wisewand API, this operation is `PATCH /v1/projects/:id` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-projects.md) for the provider-specific parameters and requirements.

