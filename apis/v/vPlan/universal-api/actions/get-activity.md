# vPlan: Get Activity



```
GET https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-activity?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vPlan/latest/actions/get-activity?${params}`, {
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
| `id` | string | yes | Activity identifier. |

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

Through the native vPlan API, this operation is `GET /activity/[:id]` (base URL `https://api.vplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity.md) for the provider-specific parameters and requirements.

