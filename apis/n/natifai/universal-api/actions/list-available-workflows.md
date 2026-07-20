# Natif.ai: List Available Workflows

Retrieves available processing workflows from Natif.ai.

```
GET https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-available-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Natif.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-available-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-available-workflows?${params}`, {
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
| `locale` | string | no | Locale/language to use for workflow labels. |
| `limit` | number | no | Maximum number of workflows to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessible_child_workflows": [
        "string"
      ],
      "any_child_deidentified": true,
      "beta": true,
      "category": "string",
      "character_set": "string",
      "customer_id": "string",
      "description": "string",
      "image": "string",
      "is_latest_architecture": true,
      "kind": "string",
      "last_training_date": "2026-05-07T12:00:00.000Z",
      "locked": true,
      "long_description": "string",
      "migration_due_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "num_of_deeper_descendant_workflows": 1,
      "num_of_inaccessible_child_workflows": 1,
      "parent_model_ahead": true,
      "parent_workflow_id": "string",
      "permissions": [
        "string"
      ],
      "preview": true,
      "retrievable_results": [
        "string"
      ],
      "shareable": true,
      "tags": [
        {}
      ],
      "training_state": "string",
      "visibility": "string",
      "workflow_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessible_child_workflows` | array<string> |  |
| `any_child_deidentified` | boolean |  |
| `beta` | boolean |  |
| `category` | string |  |
| `character_set` | string |  |
| `customer_id` | string |  |
| `description` | string |  |
| `image` | string |  |
| `is_latest_architecture` | boolean |  |
| `kind` | string |  |
| `last_training_date` | date |  |
| `locked` | boolean |  |
| `long_description` | string |  |
| `migration_due_at` | date |  |
| `name` | string |  |
| `num_of_deeper_descendant_workflows` | number |  |
| `num_of_inaccessible_child_workflows` | number |  |
| `parent_model_ahead` | boolean |  |
| `parent_workflow_id` | string |  |
| `permissions` | array<string> |  |
| `preview` | boolean |  |
| `retrievable_results` | array<string> |  |
| `shareable` | boolean |  |
| `tags` | array<object> |  |
| `training_state` | string |  |
| `visibility` | string |  |
| `workflow_id` | string |  |

## Native endpoint

Through the native Natif.ai API, this operation is `GET /processing/workflows` (base URL `https://api.natif.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-workflows.md) for the provider-specific parameters and requirements.

