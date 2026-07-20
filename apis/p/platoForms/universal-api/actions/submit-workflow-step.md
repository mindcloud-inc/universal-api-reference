# PlatoForms: Submit Workflow Step

Creates a workflow step submission in PlatoForms.

```
POST https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/submit-workflow-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/submit-workflow-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflow_identifier": "string",
  "previous_submission_identifier": "string",
  "submit_data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/submit-workflow-step', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflow_identifier": "string",
    "previous_submission_identifier": "string",
    "submit_data[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflow_identifier` | string | yes |  |
| `previous_submission_identifier` | string | yes |  |
| `submit_data[]` | array<object> | yes | Array of form field submissions |
| `sync` | boolean | no | Wait for PDF generation before responding (not recommended) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "add_ons": {},
      "attachments": {},
      "attachments_zip": {},
      "csv": {},
      "form": {},
      "form_invitation_id": "string",
      "form_invitation_link_id": "https://example.com",
      "id": "string",
      "ip_address": "string",
      "language_code": "string",
      "notifications": {},
      "pdf": {},
      "published_form_revision": 1,
      "sign_certificate": {},
      "submission_datetime_conversion": "string",
      "submit_date": "2026-05-07T12:00:00.000Z",
      "submit_form_sharing_creator_url": "https://example.com",
      "submit_form_sharing_url": "https://example.com",
      "submit_form_url": "https://example.com",
      "submit_revision": 1,
      "submitter": {},
      "user_agent": "string",
      "workflow_id": "string",
      "workflow_next_step_api_url": "https://example.com",
      "workflow_next_step_url": "https://example.com",
      "workflow_step_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `add_ons` | object |  |
| `attachments` | object |  |
| `attachments_zip` | object |  |
| `csv` | object |  |
| `form` | object |  |
| `form_invitation_id` | string |  |
| `form_invitation_link_id` | string |  |
| `id` | string |  |
| `ip_address` | string |  |
| `language_code` | string |  |
| `notifications` | object |  |
| `pdf` | object |  |
| `published_form_revision` | number |  |
| `sign_certificate` | object |  |
| `submission_datetime_conversion` | string |  |
| `submit_date` | date |  |
| `submit_form_sharing_creator_url` | string |  |
| `submit_form_sharing_url` | string |  |
| `submit_form_url` | string |  |
| `submit_revision` | number |  |
| `submitter` | object |  |
| `user_agent` | string |  |
| `workflow_id` | string |  |
| `workflow_next_step_api_url` | string |  |
| `workflow_next_step_url` | string |  |
| `workflow_step_id` | string |  |

## Native endpoint

Through the native PlatoForms API, this operation is `POST /workflow/submit/{{workflow_identifier}}/{{previous_submission_identifier}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-workflow-step.md) for the provider-specific parameters and requirements.

