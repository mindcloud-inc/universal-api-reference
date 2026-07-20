# Nautical: List Customers

Retrieves a list of customers from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-customers?${params}`, {
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
      "data": {
        "customers": {
          "edges": [
            {
              "node": {
                "companyName": "Ava Chen",
                "email": "ava@example.com",
                "firstName": "Ava",
                "id": "string",
                "lastName": "Chen"
              }
            }
          ],
          "pageInfo": {
            "endCursor": "string",
            "hasNextPage": true
          }
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
| `data.customers.edges[].node.companyName` | string |  |
| `data.customers.edges[].node.email` | string |  |
| `data.customers.edges[].node.firstName` | string |  |
| `data.customers.edges[].node.id` | string |  |
| `data.customers.edges[].node.lastName` | string |  |
| `data.customers.pageInfo.endCursor` | string |  |
| `data.customers.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

