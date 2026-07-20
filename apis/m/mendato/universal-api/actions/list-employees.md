# Mendato: List Employees



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-employees?${params}`, {
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
| `variables` | object | no | GraphQL variables object for the Mendato employees query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employees": {
        "edges": [
          {
            "node": {
              "city": "string",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "email": "ava@example.com",
              "firstName": "Ava",
              "fullPersonnelNumber": "string",
              "id": "string",
              "lastName": "Chen",
              "phone": "string",
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
| `employees.edges[].node.city` | string |  |
| `employees.edges[].node.createdAt` | date |  |
| `employees.edges[].node.email` | string |  |
| `employees.edges[].node.firstName` | string |  |
| `employees.edges[].node.fullPersonnelNumber` | string |  |
| `employees.edges[].node.id` | string |  |
| `employees.edges[].node.lastName` | string |  |
| `employees.edges[].node.phone` | string |  |
| `employees.edges[].node.status` | string |  |
| `employees.pageInfo.endCursor` | string |  |
| `employees.pageInfo.hasNextPage` | boolean |  |
| `employees.pageInfo.hasPreviousPage` | boolean |  |
| `employees.pageInfo.startCursor` | string |  |
| `employees.totalCount` | number |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

