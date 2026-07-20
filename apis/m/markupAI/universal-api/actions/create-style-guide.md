# Markup AI: Create Style Guide

Creates a new style guide in Markup AI.

```
POST https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-style-guide
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-style-guide" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUpload": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/create-style-guide', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUpload": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUpload` | file | yes | Style guide file to upload. |
| `name` | string | yes | Name for the style guide. |
| `baseStyleGuide` | string | no | Optional base style guide identifier or preset. |
| `terminologyDomainIds[]` | array<string> | no | Optional terminology domain IDs to associate with the style guide. |

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
| `base_style_guide_type` | string | The base style guide type that this style guide extends. |
| `created_at` | date | The UTC date and time the style guide was created. |
| `created_by` | string | The ID of the user who created the style guide. |
| `has_tone_prompt` | boolean | Whether this style guide has a tone prompt defined. |
| `id` | string | Unique identifier of the style guide. |
| `name` | string | The name of the style guide. |
| `status` | string | The status of the submitted style guide. |
| `summary` | string | User-friendly summary of the style guide's contents and characteristics. |
| `terminology_domain_ids` | array<string> | List of terminology domain IDs associated with the style guide. |
| `updated_at` | date | The UTC datetime that the style guide was last updated. |
| `updated_by` | string | The ID of the user who last updated the style guide. |

## Native endpoint

Through the native Markup AI API, this operation is `POST /v1/style-guides` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-style-guide.md) for the provider-specific parameters and requirements.

