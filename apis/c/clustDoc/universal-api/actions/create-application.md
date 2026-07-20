# ClustDoc: Create Application



```
POST https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact.email": "ava@example.com",
  "contact.firstname": "Codex",
  "contact.lastname": "Dossier",
  "template_id": "373355"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/create-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact.email": "ava@example.com",
    "contact.firstname": "Codex",
    "contact.lastname": "Dossier",
    "template_id": "373355"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact.email` | string | yes | Primary contact email for the application. |
| `contact.firstname` | string | yes | Primary contact first name. Default: `Codex`. |
| `contact.lastname` | string | yes | Primary contact last name. Default: `Dossier`. |
| `template_id` | string | yes | The template ID used to create the application. Default: `373355`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {},
      "count_eligible_items": 1,
      "count_missing_items": 1,
      "created_at": "string",
      "dossier_items": [
        {}
      ],
      "form_fields": [
        {}
      ],
      "id": 1,
      "is_late": true,
      "progress_percentage": 1,
      "public_url": "https://example.com",
      "secured_list_url": "https://example.com",
      "stakeholders": [
        {}
      ],
      "status": "string",
      "status_color": "string",
      "status_string": "string",
      "status_string_full": "string",
      "team": {},
      "template": {},
      "template_id": 1,
      "title": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object | The primary contact for the application. |
| `count_eligible_items` | number | The number of eligible items. |
| `count_missing_items` | number | The number of missing items. |
| `created_at` | string | When the application was created. |
| `dossier_items` | array<object> | Application checklist items. |
| `form_fields` | array<object> | Submitted form field values. |
| `id` | number | The created Clustdoc application ID. |
| `is_late` | boolean | Whether the application is late. |
| `progress_percentage` | number | The application completion percentage. |
| `public_url` | string | The public application URL. |
| `secured_list_url` | string | The secured list URL. |
| `stakeholders` | array<object> | Stakeholders associated with the application. |
| `status` | string | The application status code. |
| `status_color` | string | The color associated with the current status. |
| `status_string` | string | The localized application status label. |
| `status_string_full` | string | The full localized application status label. |
| `team` | object | The owning team. |
| `template` | object | The source template. |
| `template_id` | number | The template ID used to create the application. |
| `title` | string | The application title. |
| `updated_at` | string | When the application was last updated. |

## Native endpoint

Through the native ClustDoc API, this operation is `POST /dossiers` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-application.md) for the provider-specific parameters and requirements.

