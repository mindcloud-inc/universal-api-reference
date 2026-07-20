# PlatoForms: List Workflow First-Step Submissions

Retrieves first-step workflow submissions from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-workflow-first-step-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-workflow-first-step-submissions?connectionId=$CONNECTION_ID&workflow_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflow_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-workflow-first-step-submissions?${params}`, {
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
| `workflow_identifier` | string | yes |  |
| `sort` | string | no | Sort order ('-submitted_date' for newest first, 'submitted_date' for oldest) |
| `page` | number | no | Page number for pagination |
| `page_size` | number | no | Number of items per page (default: 50, max: 200) |
| `include_metadata` | boolean | no | Include submission metadata (date) - default: true |

## Response

```json
{
  "success": true,
  "data": [
    {
      "first_step_submissions": [
        {}
      ],
      "has_next": true,
      "has_previous": true,
      "page": 1,
      "page_size": 1,
      "total_count": 1,
      "workflow_identifier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `first_step_submissions` | array<object> |  |
| `has_next` | boolean |  |
| `has_previous` | boolean |  |
| `page` | number |  |
| `page_size` | number |  |
| `total_count` | number |  |
| `workflow_identifier` | string |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /workflow/{{workflow_identifier}}/submissions/ids/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-first-step-submissions.md) for the provider-specific parameters and requirements.

