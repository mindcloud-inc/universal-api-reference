# Extruct AI: List Discovery Tasks

Retrieves discovery tasks from Extruct AI.

```
GET https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/list-discovery-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/list-discovery-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/list-discovery-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "autoDataSources": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "criteria": [
        {}
      ],
      "dataSources": [
        "string"
      ],
      "desiredNumResults": 1,
      "id": "string",
      "isExhausted": true,
      "numResults": 1,
      "numResultsDiscovered": 1,
      "numResultsEnriched": 1,
      "numResultsEvaluated": 1,
      "query": "string",
      "status": "string",
      "tableId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoDataSources` | boolean |  |
| `createdAt` | date |  |
| `criteria` | array<object> |  |
| `dataSources` | array<string> |  |
| `desiredNumResults` | number |  |
| `id` | string |  |
| `isExhausted` | boolean |  |
| `numResults` | number |  |
| `numResultsDiscovered` | number |  |
| `numResultsEnriched` | number |  |
| `numResultsEvaluated` | number |  |
| `query` | string |  |
| `status` | string |  |
| `tableId` | string |  |

## Native endpoint

Through the native Extruct AI API, this operation is `GET /v1/discovery_tasks` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-discovery-tasks.md) for the provider-specific parameters and requirements.

