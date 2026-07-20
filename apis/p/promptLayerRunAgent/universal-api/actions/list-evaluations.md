# PromptLayer Run Agent: List Evaluations

Retrieves evaluations from PromptLayer.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-evaluations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-evaluations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/list-evaluations?${params}`, {
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
| `name` | string | no | Search for evaluations by name with a case-insensitive partial match. Example: `MindCloud Stage 3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "evaluations": [
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
| `evaluations` | array<object> |  |
| `has_next` | boolean |  |
| `has_prev` | boolean |  |
| `message` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `per_page` | number |  |
| `success` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /api/public/v2/evaluations` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-evaluations.md) for the provider-specific parameters and requirements.

