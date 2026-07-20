# Markup AI: Get Style Guide

Retrieves style guide details from Markup AI.

```
GET https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-style-guide
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Markup AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-style-guide?connectionId=$CONNECTION_ID&styleGuideId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "styleGuideId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/get-style-guide?${params}`, {
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
| `styleGuideId` | string | yes | UUID of the style guide. |

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

Through the native Markup AI API, this operation is `GET /v1/style-guides/:style_guide_id` (base URL `https://api.markup.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-style-guide.md) for the provider-specific parameters and requirements.

