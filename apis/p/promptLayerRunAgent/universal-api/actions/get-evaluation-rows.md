# PromptLayer Run Agent: Get Evaluation Rows

Retrieves rows from a PromptLayer evaluation.

```
GET https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-evaluation-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-evaluation-rows?connectionId=$CONNECTION_ID&limit=25&offset=0&evaluationId=45406" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "evaluationId": "45406"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/get-evaluation-rows?${params}`, {
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
| `evaluationId` | number | yes | ID of the evaluation report to retrieve rows from. Example: `45406`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "columns": [
        "string"
      ],
      "message": "string",
      "page": 1,
      "pages": 1,
      "per_page": 1,
      "rows": [
        [
          "string"
        ]
      ],
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
| `columns` | array<string> |  |
| `message` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `per_page` | number |  |
| `rows` | array<array> |  |
| `success` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native PromptLayer Run Agent API, this operation is `GET /api/public/v2/evaluations/:evaluationId/rows` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-evaluation-rows.md) for the provider-specific parameters and requirements.

