# Markup AI: Update Style Guide

Updates an existing style guide in Markup AI.

```
PUT https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/update-style-guide
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/update-style-guide" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "styleGuideId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/update-style-guide', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "styleGuideId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `styleGuideId` | string | yes | UUID of the style guide to update. |
| `name` | string | no | Updated style guide name. |
| `terminologyDomainIds[]` | array<string> | no | Updated terminology domain IDs for the style guide. |

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

Through the native Markup AI API, this operation is `PATCH /v1/style-guides/:style_guide_id` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-style-guide.md) for the provider-specific parameters and requirements.

