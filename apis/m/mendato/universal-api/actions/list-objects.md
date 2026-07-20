# Mendato: List Objects



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/list-objects?${params}`, {
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
| `variables` | object | no | GraphQL variables object for the Mendato objects query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "objects": {
        "edges": [
          {
            "node": {
              "city": "string",
              "createdAt": "2026-05-07T12:00:00.000Z",
              "email": "ava@example.com",
              "id": "string",
              "name": "Ava Chen",
              "number": 1,
              "phone": "string",
              "streetAddress": "string",
              "zip": "string"
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
| `objects.edges[].node.city` | string |  |
| `objects.edges[].node.createdAt` | date |  |
| `objects.edges[].node.email` | string |  |
| `objects.edges[].node.id` | string |  |
| `objects.edges[].node.name` | string |  |
| `objects.edges[].node.number` | number |  |
| `objects.edges[].node.phone` | string |  |
| `objects.edges[].node.streetAddress` | string |  |
| `objects.edges[].node.zip` | string |  |
| `objects.pageInfo.endCursor` | string |  |
| `objects.pageInfo.hasNextPage` | boolean |  |
| `objects.pageInfo.hasPreviousPage` | boolean |  |
| `objects.pageInfo.startCursor` | string |  |
| `objects.totalCount` | number |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-objects.md) for the provider-specific parameters and requirements.

