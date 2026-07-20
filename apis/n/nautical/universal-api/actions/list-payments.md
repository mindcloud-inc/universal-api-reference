# Nautical: List Payments

Retrieves a list of payments from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-payments?${params}`, {
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
        "payments": {
          "edges": [
            {
              "node": {
                "created": "string",
                "gateway": "string",
                "id": "string",
                "isActive": true,
                "modified": "string"
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
| `data.payments.edges[].node.created` | string |  |
| `data.payments.edges[].node.gateway` | string |  |
| `data.payments.edges[].node.id` | string |  |
| `data.payments.edges[].node.isActive` | boolean |  |
| `data.payments.edges[].node.modified` | string |  |
| `data.payments.pageInfo.endCursor` | string |  |
| `data.payments.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

