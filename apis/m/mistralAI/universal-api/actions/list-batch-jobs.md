# Mistral AI: List Batch Jobs

Retrieves batch jobs from Mistral AI.

```
GET https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/list-batch-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mistral AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/list-batch-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mistralAI/latest/actions/list-batch-jobs?${params}`, {
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
| `model` | string | no | Optional model filter. |
| `agentId` | string | no | Optional agent filter. |
| `metadata` | object | no | Optional metadata filter object. |
| `createdAfter` | string | no | Only return jobs created after this timestamp. |
| `createdByMe` | boolean | no | Only return jobs created by the current user. |
| `status[]` | array<string> | no | Optional batch job status filter list. |
| `orderBy` | string | no | Sort order for batch jobs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "object": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `object` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Mistral AI API, this operation is `GET /v1/batch/jobs` (base URL `https://api.mistral.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-batch-jobs.md) for the provider-specific parameters and requirements.

