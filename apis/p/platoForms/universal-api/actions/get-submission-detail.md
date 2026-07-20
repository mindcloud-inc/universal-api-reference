# PlatoForms: Get Submission Detail

Retrieves detailed submission data from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-submission-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-submission-detail?connectionId=$CONNECTION_ID&submission_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submission_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-submission-detail?${params}`, {
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
| `submission_identifier` | string | yes |  |
| `create_shared_urls` | boolean | no | Generate temporary shared download URLs for PDFs and attachments |

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
      "submit_data": [
        {}
      ],
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
| `submit_data` | array<object> |  |
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

Through the native PlatoForms API, this operation is `GET /submission/{{submission_identifier}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-submission-detail.md) for the provider-specific parameters and requirements.

