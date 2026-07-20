# Orbit AI (Forms): Delete Form



```
DELETE https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/delete-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orbit AI (Forms) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/delete-form?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orbitAIForms/latest/actions/delete-form?${params}`, {
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
| `id` | string | no | The Orbit form UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "settings": {},
      "slug": "string",
      "status": "string",
      "title": "string",
      "type": "string",
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
| `description` | string |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `settings` | object |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Orbit AI (Forms) API, this operation is `DELETE /api/v1/forms/:id` (base URL `https://orbitforms.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form.md) for the provider-specific parameters and requirements.

