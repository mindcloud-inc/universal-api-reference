# PlatoForms: List Workflow Execution Trees

Retrieves workflow execution trees from PlatoForms.

```
GET https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-workflow-execution-trees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-workflow-execution-trees?connectionId=$CONNECTION_ID&workflow_identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflow_identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/list-workflow-execution-trees?${params}`, {
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
| `page` | number | no | Page number |
| `results_per_page` | number | no | Items per page (max 100) |
| `status` | string | no | Filter by completion status |
| `sort` | string | no | Sort order |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "page": 1,
      "results_per_page": 1,
      "total_count": 1,
      "total_pages": 1,
      "total_steps": 1,
      "workflow_id": "string",
      "workflow_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `page` | number |  |
| `results_per_page` | number |  |
| `total_count` | number |  |
| `total_pages` | number |  |
| `total_steps` | number |  |
| `workflow_id` | string |  |
| `workflow_name` | string |  |

## Native endpoint

Through the native PlatoForms API, this operation is `GET /workflow/{{workflow_identifier}}/trees/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflow-execution-trees.md) for the provider-specific parameters and requirements.

