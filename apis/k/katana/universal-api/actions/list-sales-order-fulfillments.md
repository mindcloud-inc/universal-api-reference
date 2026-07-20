# Katana: List Sales Order Fulfillments

Lists sales order fulfillments in Katana.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-sales-order-fulfillments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-sales-order-fulfillments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-sales-order-fulfillments?${params}`, {
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
| `salesOrderId` | number | no | Filters sales order fulfillments by a sales order id |
| `pickedDateMin` | string | no | Filters sales order fulfillments by a picked date min |
| `trackingNumber` | string | no | Filters sales order fulfillments by a tracking number |
| `trackingUrl` | string | no | Filters sales order fulfillments by a tracking url |
| `trackingCarrier` | string | no | Filters sales order fulfillments by a tracking carrier |
| `trackingMethod` | string | no | Filters sales order fulfillments by a tracking method |
| `status` | string | no | Filters sales order fulfillments by a status |
| `includeDeleted` | boolean | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `createdAtMin` | string | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `createdAtMax` | string | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updatedAtMin` | string | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updatedAtMax` | string | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversionDate": "string",
      "conversionRate": 1,
      "id": 1,
      "invoiceStatus": "string",
      "packerId": 1,
      "pickedDate": "string",
      "salesOrderFulfillmentRows": [
        {
          "batchTransactions": [
            {
              "batchId": 1,
              "quantity": 1
            }
          ],
          "id": 1,
          "quantity": 1,
          "salesOrderRowId": 1,
          "serialNumbers": [
            1
          ]
        }
      ],
      "salesOrderId": 1,
      "status": "string",
      "trackingCarrier": "string",
      "trackingMethod": "string",
      "trackingNumber": "string",
      "trackingUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversionDate` | string |  |
| `conversionRate` | number |  |
| `id` | number |  |
| `invoiceStatus` | string |  |
| `packerId` | number |  |
| `pickedDate` | string |  |
| `salesOrderFulfillmentRows` | array<object> |  |
| `salesOrderFulfillmentRows[].batchTransactions` | array<object> |  |
| `salesOrderFulfillmentRows[].batchTransactions[].batchId` | number |  |
| `salesOrderFulfillmentRows[].batchTransactions[].quantity` | number |  |
| `salesOrderFulfillmentRows[].id` | number |  |
| `salesOrderFulfillmentRows[].quantity` | number |  |
| `salesOrderFulfillmentRows[].salesOrderRowId` | number |  |
| `salesOrderFulfillmentRows[].serialNumbers` | array<number> |  |
| `salesOrderId` | number |  |
| `status` | string |  |
| `trackingCarrier` | string |  |
| `trackingMethod` | string |  |
| `trackingNumber` | string |  |
| `trackingUrl` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /sales_order_fulfillments` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-order-fulfillments.md) for the provider-specific parameters and requirements.

