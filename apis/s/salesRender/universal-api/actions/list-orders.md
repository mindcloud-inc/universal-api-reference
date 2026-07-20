# SalesRender: List Orders

Retrieves orders from SalesRender.

```
GET https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-orders?connectionId=$CONNECTION_ID&query=query%20%7B%20ordersFetcher%20%7B%20orders%20%7B%20id%20createdAt%20updatedAt%20exception%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { ordersFetcher { orders { id createdAt updatedAt exception } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/list-orders?${params}`, {
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
| `query` | string | yes | GraphQL query to execute against SalesRender. Default: `query {\n  ordersFetcher {\n    orders {\n      id\n      createdAt\n      updatedAt\n      exception\n    }\n  }\n}`. Example: `query { ordersFetcher { orders { id createdAt updatedAt exception } } }`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | Optional GraphQL variables object. Default: `{}`. Example: `Optional JSON variables string`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "ordersFetcher": {
          "orders": [
            {
              "createdAt": "2026-05-07T12:00:00.000Z",
              "exception": "string",
              "id": "string",
              "updatedAt": "2026-05-07T12:00:00.000Z"
            }
          ]
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
| `data.ordersFetcher.orders[].createdAt` | date | Order creation timestamp. |
| `data.ordersFetcher.orders[].exception` | string | Order exception text, if any. |
| `data.ordersFetcher.orders[].id` | string | Order ID. |
| `data.ordersFetcher.orders[].updatedAt` | date | Order update timestamp. |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

