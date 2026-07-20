# Paperless: Get Template



```
GET https://connect.mindcloud.co/v1/universal/paperless/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paperless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperless/latest/actions/get-template?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperless/latest/actions/get-template?${params}`, {
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
| `id` | number | yes | The Paperless template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_locale_settings": [
        {}
      ],
      "created_at": "string",
      "creator_id": 1,
      "delegation_allowed": true,
      "description": "string",
      "forwarding_allowed": true,
      "has_inputs": true,
      "id": 1,
      "localized_attributes": {},
      "name": "Ava Chen",
      "original_content_locale": "string",
      "page_count": 1,
      "participant_completed_redirect_url": "https://example.com",
      "participation_flow_id": 1,
      "reminder_settings": {},
      "rendering_locale": "string",
      "settings": {},
      "styles": {},
      "updated_at": "string",
      "usage_count": 1,
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_locale_settings` | array<object> |  |
| `created_at` | string |  |
| `creator_id` | number |  |
| `delegation_allowed` | boolean |  |
| `description` | string |  |
| `forwarding_allowed` | boolean |  |
| `has_inputs` | boolean |  |
| `id` | number |  |
| `localized_attributes` | object |  |
| `name` | string |  |
| `original_content_locale` | string |  |
| `page_count` | number |  |
| `participant_completed_redirect_url` | string |  |
| `participation_flow_id` | number |  |
| `reminder_settings` | object |  |
| `rendering_locale` | string |  |
| `settings` | object |  |
| `styles` | object |  |
| `updated_at` | string |  |
| `usage_count` | number |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Paperless API, this operation is `GET /templates/:id` (base URL `https://app.paperless.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

