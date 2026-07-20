# Mendato: List Customers



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-customers?${params}`, {
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
| `variables` | object | no | Optional GraphQL variables object for after, before, first, last, and query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customers": {
        "edges": [
          {
            "node": {
              "addressSupplement": "string",
              "companyName": "Ava Chen",
              "firstName": "Ava",
              "id": "string",
              "lastName": "Chen",
              "number": 1,
              "salutation": "string",
              "type": "string"
            }
          }
        ],
        "pageInfo": {
          "endCursor": "string",
          "hasNextPage": true,
          "hasPreviousPage": true,
          "startCursor": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers.edges[].node.addressSupplement` | string |  |
| `customers.edges[].node.companyName` | string |  |
| `customers.edges[].node.firstName` | string |  |
| `customers.edges[].node.id` | string |  |
| `customers.edges[].node.lastName` | string |  |
| `customers.edges[].node.number` | number |  |
| `customers.edges[].node.salutation` | string |  |
| `customers.edges[].node.type` | string |  |
| `customers.pageInfo.endCursor` | string |  |
| `customers.pageInfo.hasNextPage` | boolean |  |
| `customers.pageInfo.hasPreviousPage` | boolean |  |
| `customers.pageInfo.startCursor` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

