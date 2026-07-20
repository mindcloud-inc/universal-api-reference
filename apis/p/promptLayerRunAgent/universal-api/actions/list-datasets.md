# PromptLayer Run Agent: List Datasets

Retrieves a list of datasets from PromptLayer.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-datasets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-datasets?${params}`, {
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
| `datasetGroupId` | number | no | Filter by specific dataset group ID. Example: `20196`. |
| `name` | string | no | Filter datasets by dataset group name. Example: `MindCloud Stage 3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Filter datasets by status: active, deleted, or all. Example: `active`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datasets": [
        {}
      ],
      "has_next": true,
      "has_prev": true,
      "message": "string",
      "page": 1,
      "pages": 1,
      "per_page": 1,
      "success": true,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasets` | array<object> |  |
| `has_next` | boolean |  |
| `has_prev` | boolean |  |
| `message` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `per_page` | number |  |
| `success` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /api/public/v2/datasets` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-datasets.md) for the provider-specific parameters and requirements.

