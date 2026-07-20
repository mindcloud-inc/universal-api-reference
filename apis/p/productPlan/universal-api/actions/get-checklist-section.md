# ProductPlan: Get Checklist Section

Retrieves a checklist section from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-checklist-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-checklist-section?connectionId=$CONNECTION_ID&id=string&launchId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "launchId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-checklist-section?${params}`, {
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
| `id` | string | yes |  |
| `launchId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "launch_id": 1,
      "name": "Ava Chen",
      "task_ids": [
        1
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | number |  |
| `launch_id` | number |  |
| `name` | string |  |
| `task_ids` | array<number> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /launches/:launch_id/checklist_sections/:id` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-checklist-section.md) for the provider-specific parameters and requirements.

