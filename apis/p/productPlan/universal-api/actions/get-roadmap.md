# ProductPlan: Get Roadmap

Retrieves a roadmap from ProductPlan.

```
GET https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-roadmap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductPlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-roadmap?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productPlan/latest/actions/get-roadmap?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_dropdown_fields": [
        {}
      ],
      "custom_text_fields": [
        {}
      ],
      "description": "string",
      "id": 1,
      "is_version": true,
      "lanes": [
        "string"
      ],
      "legends": [
        "string"
      ],
      "name": "Ava Chen",
      "owner": {},
      "permission": "string",
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
| `created_at` | date |  |
| `custom_dropdown_fields` | array<object> |  |
| `custom_text_fields` | array<object> |  |
| `description` | string |  |
| `id` | number |  |
| `is_version` | boolean |  |
| `lanes` | array<string> |  |
| `legends` | array<string> |  |
| `name` | string |  |
| `owner` | object |  |
| `permission` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native ProductPlan API, this operation is `GET /roadmaps/:id` (base URL `https://app.productplan.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-roadmap.md) for the provider-specific parameters and requirements.

