# SalesRender: Update Order

Updates an existing order in SalesRender.

```
PUT https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesRender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation UpdateOrder($input: UpdateOrderInput!) {\n  orderMutation {\n    updateOrder(input: $input) {\n      id\n      createdAt\n      updatedAt\n      exception\n    }\n  }\n}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesRender/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation UpdateOrder($input: UpdateOrderInput!) {\n  orderMutation {\n    updateOrder(input: $input) {\n      id\n      createdAt\n      updatedAt\n      exception\n    }\n  }\n}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | GraphQL variables object. Set `input` to a valid UpdateOrderInput payload. Default: `{"input":{}}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | GraphQL mutation to execute. Default: `mutation UpdateOrder($input: UpdateOrderInput!) {\n  orderMutation {\n    updateOrder(input: $input) {\n      id\n      createdAt\n      updatedAt\n      exception\n    }\n  }\n}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "orderMutation": {
          "updateOrder": {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "exception": "string",
            "id": "string",
            "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `data.orderMutation.updateOrder.createdAt` | date |  |
| `data.orderMutation.updateOrder.exception` | string |  |
| `data.orderMutation.updateOrder.id` | string |  |
| `data.orderMutation.updateOrder.updatedAt` | date |  |

## Native endpoint

Through the native SalesRender API, this operation is `POST :companyId/CRM` (base URL `https://de.backend.salesrender.com/companies`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

