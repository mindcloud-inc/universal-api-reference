# PlatoForms: Get Draft Submission Detail

Retrieves draft submission details from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-draft-submission-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-draft-submission-detail?connectionId=$CONNECTION_ID&submission_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submission_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/get-draft-submission-detail?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {},
      "attachments_zip": {},
      "draft_url": "https://example.com",
      "form": {},
      "id": "string",
      "ip_address": "string",
      "published_form_revision": 1,
      "saved_date": "2026-05-07T12:00:00.000Z",
      "submit_data": [
        {}
      ],
      "submitter": {},
      "user_agent": "string",
      "workflow_id": "string",
      "workflow_step_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | object |  |
| `attachments_zip` | object |  |
| `draft_url` | string |  |
| `form` | object |  |
| `id` | string |  |
| `ip_address` | string |  |
| `published_form_revision` | number |  |
| `saved_date` | date |  |
| `submit_data` | array<object> |  |
| `submitter` | object |  |
| `user_agent` | string |  |
| `workflow_id` | string |  |
| `workflow_step_id` | string |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /submission/draft/{{submission_identifier}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-draft-submission-detail.md) for the provider-specific parameters and requirements.

