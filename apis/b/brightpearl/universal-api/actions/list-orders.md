# Brightpearl: List Orders



```
GET https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brightpearl `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-orders?${params}`, {
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
      "contactId": 1,
      "createdById": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customerRef": "string",
      "deliveryDate": "2026-05-07T12:00:00.000Z",
      "departmentId": 1,
      "externalRef": "string",
      "installedIntegrationInstanceId": 1,
      "orderId": 1,
      "orderPaymentStatusId": 1,
      "orderShippingStatusId": 1,
      "orderStatusId": 1,
      "orderStockStatusId": 1,
      "orderTypeId": 1,
      "parentOrderId": 1,
      "staffOwnerContactId": 1,
      "taxDate": "2026-05-07T12:00:00.000Z",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number | The ID of the Contact. Can be used to recover all information about a contact by issuing a Contact GET. |
| `createdById` | number | The ID of the Staff member who created this order. |
| `createdOn` | date | The date the Order was created. |
| `customerRef` | string | The customer reference for the order. |
| `deliveryDate` | date | The date the delivery is set for. |
| `departmentId` | number | The ID of the department the Order is associated with. |
| `externalRef` | string | The external reference for the order |
| `installedIntegrationInstanceId` | number | The integration instance this order is associated with |
| `orderId` | number | The ID of the Order. Can be used to retrieve all order information using Order Get. |
| `orderPaymentStatusId` | number | The payment status ID of the order |
| `orderShippingStatusId` | number | The shipping status ID of the order |
| `orderStatusId` | number | The ID of the Order status. Description can be found in the report reference data. |
| `orderStockStatusId` | number | The ID of the Order stock status. Description can be found in the report reference data. |
| `orderTypeId` | number | The ID of the Order Type. See report reference data for description. |
| `parentOrderId` | number | The ID of the order's parent. Orders have a parent when they are linked to another order, for example a sales credit linked to a sales order. |
| `staffOwnerContactId` | number | The ID of the staff member who is assigned to the order. |
| `taxDate` | date | The tax date of the order. |
| `updatedOn` | date | The date the Order was updated. |
| `warehouseId` | number | The ID of the warehouse. Can be used to retrieve all orders for a given warehouse ID. |

## Native endpoint

Through the native Brightpearl API, this operation is `GET /order-service/order-search` (base URL `https://{{credentials.apiDomain}}/public-api/{{credentials.account}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

