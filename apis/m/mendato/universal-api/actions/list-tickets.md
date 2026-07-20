# Mendato: List Tickets



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-tickets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-tickets?${params}`, {
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
| `variables` | object | no | GraphQL variables object for the Mendato tickets query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tickets": {
        "edges": [
          {
            "node": {
              "completedAt": "2026-05-07T12:00:00.000Z",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "description": "string",
              "dueDate": "2026-05-07T12:00:00.000Z",
              "id": "string",
              "inputChannel": "string",
              "isPublic": true,
              "location": "string",
              "number": 1,
              "priority": "string",
              "rejectedAt": "2026-05-07T12:00:00.000Z",
              "status": "string",
              "type": "string"
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
| `tickets.edges[].node.completedAt` | date |  |
| `tickets.edges[].node.createdAt` | date |  |
| `tickets.edges[].node.description` | string |  |
| `tickets.edges[].node.dueDate` | date |  |
| `tickets.edges[].node.id` | string |  |
| `tickets.edges[].node.inputChannel` | string |  |
| `tickets.edges[].node.isPublic` | boolean |  |
| `tickets.edges[].node.location` | string |  |
| `tickets.edges[].node.number` | number |  |
| `tickets.edges[].node.priority` | string |  |
| `tickets.edges[].node.rejectedAt` | date |  |
| `tickets.edges[].node.status` | string |  |
| `tickets.edges[].node.type` | string |  |
| `tickets.pageInfo.endCursor` | string |  |
| `tickets.pageInfo.hasNextPage` | boolean |  |
| `tickets.pageInfo.hasPreviousPage` | boolean |  |
| `tickets.pageInfo.startCursor` | string |  |
| `tickets.totalCount` | number |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tickets.md) for the provider-specific parameters and requirements.

