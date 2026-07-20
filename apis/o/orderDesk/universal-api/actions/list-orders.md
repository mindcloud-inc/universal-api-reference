# Order Desk: List Orders

Retrieves orders from Order Desk.

```
GET https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/list-orders?${params}`, {
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
| `folderId` | string | no | Filter to a specific folder ID or comma-separated folder IDs. |
| `folderName` | string | no | Filter to a folder by exact folder name. |
| `sourceId` | string | no | Filter to a specific source ID. |
| `sourceName` | string | no | Filter to a specific source name. |
| `searchStartDate` | string | no | UTC start date for added orders, in Order Desk date-time format. |
| `searchEndDate` | string | no | UTC end date for added orders, in Order Desk date-time format. |
| `modifiedStartDate` | string | no | UTC start date for modified orders, in Order Desk date-time format. |
| `modifiedEndDate` | string | no | UTC end date for modified orders, in Order Desk date-time format. |
| `email` | string | no | Filter by customer email address. |
| `customerId` | string | no | Filter by originating customer ID. |
| `shippingLastName` | string | no | Filter by shipping last name. |
| `getOrderHistory` | boolean | no | Set to true to include order history in results. |
| `orderBy` | string | no | Order field to sort by. Defaults to date_added. |
| `order` | string | no | Sort direction, ASC or DESC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {},
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "discountTotal": 1,
      "email": "ava@example.com",
      "folderId": 1,
      "id": "string",
      "orderItems": [
        {}
      ],
      "orderTotal": 1,
      "paymentStatus": "string",
      "paymentType": "string",
      "productTotal": 1,
      "quantityTotal": 1,
      "shipping": {},
      "shippingMethod": "string",
      "shippingTotal": 1,
      "sourceId": "string",
      "sourceName": "Ava Chen",
      "taxTotal": 1,
      "weightTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | object | Customer address details. |
| `dateAdded` | date | Order creation timestamp in UTC. |
| `dateUpdated` | date | Last update timestamp in UTC. |
| `discountTotal` | number | Discount total. |
| `email` | string | Customer email address. |
| `folderId` | number | Current folder ID. |
| `id` | string | Order Desk internal order ID. |
| `orderItems` | array<object> | Order line items. |
| `orderTotal` | number | Final order total. |
| `paymentStatus` | string | Payment status. |
| `paymentType` | string | Payment method type. |
| `productTotal` | number | Product subtotal. |
| `quantityTotal` | number | Total quantity across order items. |
| `shipping` | object | Shipping address details. |
| `shippingMethod` | string | Shipping method name. |
| `shippingTotal` | number | Shipping total. |
| `sourceId` | string | Order source ID. |
| `sourceName` | string | Order source name. |
| `taxTotal` | number | Tax total. |
| `weightTotal` | number | Total order weight. |

## Native endpoint

Through the native Order Desk API, this operation is `GET /orders` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

