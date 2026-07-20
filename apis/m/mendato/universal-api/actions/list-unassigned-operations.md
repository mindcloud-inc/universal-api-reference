# Mendato: List Unassigned Operations



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-unassigned-operations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-unassigned-operations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-unassigned-operations?${params}`, {
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
| `variables` | object | no | GraphQL variables object for the Mendato unassigned operations query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "unassignedOperations": {
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
| `unassignedOperations.edges[].node.createdAt` | date |  |
| `unassignedOperations.edges[].node.duration` | number |  |
| `unassignedOperations.edges[].node.executionEndDate` | date |  |
| `unassignedOperations.edges[].node.executionEndTime` | string |  |
| `unassignedOperations.edges[].node.executionStartDate` | date |  |
| `unassignedOperations.edges[].node.executionStartTime` | string |  |
| `unassignedOperations.edges[].node.id` | string |  |
| `unassignedOperations.edges[].node.instructions` | string |  |
| `unassignedOperations.edges[].node.isExecuted` | boolean |  |
| `unassignedOperations.edges[].node.missingExecutors` | number |  |
| `unassignedOperations.edges[].node.requiredExecutors` | number |  |
| `unassignedOperations.edges[].node.toDos[]` | string |  |
| `unassignedOperations.pageInfo.endCursor` | string |  |
| `unassignedOperations.pageInfo.hasNextPage` | boolean |  |
| `unassignedOperations.pageInfo.hasPreviousPage` | boolean |  |
| `unassignedOperations.pageInfo.startCursor` | string |  |
| `unassignedOperations.totalCount` | number |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unassigned-operations.md) for the provider-specific parameters and requirements.

