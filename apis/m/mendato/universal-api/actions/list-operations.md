# Mendato: List Operations



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-operations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-operations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-operations?${params}`, {
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
| `variables` | object | no | GraphQL variables object for the Mendato operations query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "operations": {
        "edges": [
          {
            "node": {
              "createdAt": "2026-05-07T12:00:00.000Z",
              "duration": 1,
              "executionEndDate": "2026-05-07T12:00:00.000Z",
              "executionEndTime": "string",
              "executionStartDate": "2026-05-07T12:00:00.000Z",
              "executionStartTime": "string",
              "id": "string",
              "instructions": "string",
              "isExecuted": true,
              "missingExecutors": 1,
              "requiredExecutors": 1,
              "toDos": [
                "string"
              ]
            }
          }
        ],
        "pageInfo": {
          "endCursor": "string",
          "hasNextPage": true,
          "hasPreviousPage": true,
          "startCursor": "string"
        },
        "totalCount": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `operations.edges[].node.createdAt` | date |  |
| `operations.edges[].node.duration` | number |  |
| `operations.edges[].node.executionEndDate` | date |  |
| `operations.edges[].node.executionEndTime` | string |  |
| `operations.edges[].node.executionStartDate` | date |  |
| `operations.edges[].node.executionStartTime` | string |  |
| `operations.edges[].node.id` | string |  |
| `operations.edges[].node.instructions` | string |  |
| `operations.edges[].node.isExecuted` | boolean |  |
| `operations.edges[].node.missingExecutors` | number |  |
| `operations.edges[].node.requiredExecutors` | number |  |
| `operations.edges[].node.toDos[]` | string |  |
| `operations.pageInfo.endCursor` | string |  |
| `operations.pageInfo.hasNextPage` | boolean |  |
| `operations.pageInfo.hasPreviousPage` | boolean |  |
| `operations.pageInfo.startCursor` | string |  |
| `operations.totalCount` | number |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-operations.md) for the provider-specific parameters and requirements.

