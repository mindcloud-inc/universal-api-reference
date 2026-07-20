# ProductPlan: Get Idea

Retrieves an idea from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-idea?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-idea?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_dropdown_fields": [
        {}
      ],
      "custom_text_fields": [
        {}
      ],
      "customer": "string",
      "description": "string",
      "id": 1,
      "idea_form_id": 1,
      "location_status": "string",
      "name": "Ava Chen",
      "opportunities_count": 1,
      "opportunity_ids": [
        1
      ],
      "source_email": "ava@example.com",
      "source_name": "Ava Chen",
      "tags": [
        "string"
      ],
      "team_ids": [
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
| `channel` | string |  |
| `created_at` | date |  |
| `custom_dropdown_fields` | array<object> |  |
| `custom_text_fields` | array<object> |  |
| `customer` | string |  |
| `description` | string |  |
| `id` | number |  |
| `idea_form_id` | number |  |
| `location_status` | string |  |
| `name` | string |  |
| `opportunities_count` | number |  |
| `opportunity_ids` | array<number> |  |
| `source_email` | string |  |
| `source_name` | string |  |
| `tags` | array<string> |  |
| `team_ids` | array<number> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /discovery/ideas/:id` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-idea.md) for the provider-specific parameters and requirements.

