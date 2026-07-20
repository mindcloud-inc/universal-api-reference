# Markup AI: List Style Guides

Retrieves style guides from Markup AI.

```
GET https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/list-style-guides
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/list-style-guides?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/list-style-guides?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "base_style_guide_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "has_tone_prompt": true,
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "summary": "string",
      "terminology_domain_ids": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "updated_by": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_style_guide_type` | string |  |
| `created_at` | date |  |
| `created_by` | string |  |
| `has_tone_prompt` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `summary` | string |  |
| `terminology_domain_ids` | array<string> |  |
| `updated_at` | date |  |
| `updated_by` | string |  |

## Native endpoint

Through the native Markup AI API, this operation is `GET /v1/style-guides` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-style-guides.md) for the provider-specific parameters and requirements.

