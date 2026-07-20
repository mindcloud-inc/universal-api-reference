# Frameshift: List Variant Filters

Retrieves a list of variant filters from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-variant-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-variant-filters?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-variant-filters?${params}`, {
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
| `projectId` | string | yes | Resource identifier for the project to access |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "category_view_order": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "filter": {
        "var_type": [
          "string"
        ]
      },
      "id": 1,
      "name": "Ava Chen",
      "project_id": 1,
      "sort_dir": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `category_view_order` | number |  |
| `created_at` | date |  |
| `description` | string |  |
| `filter.var_type[]` | string |  |
| `id` | number |  |
| `name` | string |  |
| `project_id` | number |  |
| `sort_dir` | string |  |
| `updated_at` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/variants/filters` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-variant-filters.md) for the provider-specific parameters and requirements.

