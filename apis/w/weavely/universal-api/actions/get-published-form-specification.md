# Weavely: Get Published Form Specification

Retrieves a published form specification from Weavely.

```
GET https://connect.mindcloud.co/v1/universal/weavely/latest/actions/get-published-form-specification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weavely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weavely/latest/actions/get-published-form-specification?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weavely/latest/actions/get-published-form-specification?${params}`, {
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
| `id` | string | yes | The unique identifier of the published form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calculatedValues": [
        {}
      ],
      "eventTriggers": [
        {}
      ],
      "formJSON": {},
      "i18n": {},
      "id": "string",
      "logicRules": [
        {}
      ],
      "name": "Ava Chen",
      "pageAttributes": {},
      "plan": "string",
      "settings": {},
      "themeJSON": {},
      "variables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculatedValues` | array<object> | Calculated field values. |
| `eventTriggers` | array<object> | Event-based triggers. |
| `formJSON` | object | Complete form structure with all pages and elements. |
| `i18n` | object | Internationalization settings. |
| `id` | string | The form unique identifier. |
| `logicRules` | array<object> | Conditional logic rules. |
| `name` | string | The form display name. |
| `pageAttributes` | object | Page metadata and SEO attributes. |
| `plan` | string | The Weavely plan tier. |
| `settings` | object | Form settings. |
| `themeJSON` | object | Theme configuration. |
| `variables` | array<object> | Auto-generated variables for input fields. |

## Native endpoint

Through the native Weavely API, this operation is `GET https://api.weavely.ai/forms/:id/client` (base URL `https://api.weavely.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-published-form-specification.md) for the provider-specific parameters and requirements.

