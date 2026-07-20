# ProductPlan: Get Bar

Retrieves a bar from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-bar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-bar?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-bar?${params}`, {
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
      "child_bar_count": 1,
      "comment_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_dropdown_fields": [
        {}
      ],
      "custom_text_fields": [
        {}
      ],
      "description": "string",
      "ends_on": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_container": true,
      "lane": "string",
      "legend": "string",
      "link_count": 1,
      "name": "Ava Chen",
      "notes": "string",
      "parent": {},
      "parked": true,
      "percent_done": 1,
      "required_by_connection_count": 1,
      "requires_connection_count": 1,
      "roadmap": {},
      "starts_on": "2026-05-07T12:00:00.000Z",
      "strategic_value": "string",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `child_bar_count` | number |  |
| `comment_count` | number |  |
| `created_at` | date |  |
| `custom_dropdown_fields` | array<object> |  |
| `custom_text_fields` | array<object> |  |
| `description` | string |  |
| `ends_on` | date |  |
| `id` | number |  |
| `is_container` | boolean |  |
| `lane` | string |  |
| `legend` | string |  |
| `link_count` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `parent` | object |  |
| `parked` | boolean |  |
| `percent_done` | number |  |
| `required_by_connection_count` | number |  |
| `requires_connection_count` | number |  |
| `roadmap` | object |  |
| `starts_on` | date |  |
| `strategic_value` | string |  |
| `tags` | array<string> |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /bars/:id` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bar.md) for the provider-specific parameters and requirements.

