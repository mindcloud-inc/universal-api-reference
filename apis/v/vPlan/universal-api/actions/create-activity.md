# vPlan: Create Activity



```
POST https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boardId": "85b9270e-b0f4-4f8c-b492-1fb8a19c984f",
  "description": "Created through MindCloud action validation",
  "name": "Codex Action Activity"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boardId": "85b9270e-b0f4-4f8c-b492-1fb8a19c984f",
    "description": "Created through MindCloud action validation",
    "name": "Codex Action Activity"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boardId` | string | yes | Board identifier for the new activity. Default: `85b9270e-b0f4-4f8c-b492-1fb8a19c984f`. |
| `description` | string | yes | Activity description. Default: `Created through MindCloud action validation`. |
| `name` | string | yes | Activity name. Default: `Codex Action Activity`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived_at": "string",
      "billable": true,
      "code": "string",
      "created_at": "string",
      "day_max_duration": 1,
      "default_duration": 1,
      "deleted_at": "string",
      "description": "string",
      "external_ref": "string",
      "hourly_rate": 1,
      "id": "string",
      "item_id": "string",
      "resource_type": "string",
      "transaction": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | string | Archive timestamp. |
| `billable` | boolean | Whether the activity is billable. |
| `code` | string | Activity code. |
| `created_at` | string | Creation timestamp. |
| `day_max_duration` | number | Maximum day duration. |
| `default_duration` | number | Default duration. |
| `deleted_at` | string | Deletion timestamp. |
| `description` | string | Activity description. |
| `external_ref` | string | External reference. |
| `hourly_rate` | number | Hourly rate. |
| `id` | string | Activity identifier. |
| `item_id` | string | Linked item identifier when present. |
| `resource_type` | string | Activity resource type. |
| `transaction` | string | Provider transaction value. |
| `updated_at` | string | Last update timestamp. |

## Native endpoint

Through the native vPlan API, this operation is `POST /activity` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

