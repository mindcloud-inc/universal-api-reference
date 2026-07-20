# Wisewand: Update a categorypages

Updates an existing category page in your Wisewand workspace.

```
PUT https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/update-a-categorypages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/update-a-categorypages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "test-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/update-a-categorypages', {
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

Through the native Wisewand API, this operation is `PATCH /v1/categorypages/:id` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-categorypages.md) for the provider-specific parameters and requirements.

