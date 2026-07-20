# Mendato: List Orders



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-orders?${params}`, {
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
| `variables` | object | no | GraphQL variables object for the Mendato orders query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": {
        "edges": [
          {
            "node": {
              "cancelledAt": "2026-05-07T12:00:00.000Z",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "endDate": "2026-05-07T12:00:00.000Z",
              "executionOnHolidays": true,
              "id": "string",
              "instructions": "string",
              "missingExecutors": 1,
              "number": 1,
              "requiredExecutors": 1,
              "startDate": "2026-05-07T12:00:00.000Z",
              "status": "string"
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
| `orders.edges[].node.cancelledAt` | date |  |
| `orders.edges[].node.createdAt` | date |  |
| `orders.edges[].node.endDate` | date |  |
| `orders.edges[].node.executionOnHolidays` | boolean |  |
| `orders.edges[].node.id` | string |  |
| `orders.edges[].node.instructions` | string |  |
| `orders.edges[].node.missingExecutors` | number |  |
| `orders.edges[].node.number` | number |  |
| `orders.edges[].node.requiredExecutors` | number |  |
| `orders.edges[].node.startDate` | date |  |
| `orders.edges[].node.status` | string |  |
| `orders.pageInfo.endCursor` | string |  |
| `orders.pageInfo.hasNextPage` | boolean |  |
| `orders.pageInfo.hasPreviousPage` | boolean |  |
| `orders.pageInfo.startCursor` | string |  |
| `orders.totalCount` | number |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

