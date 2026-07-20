# Katana: Update Sales Order

Updates an existing sales order in Katana.

```
PUT https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Sales order id |
| `orderNo` | string | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `customerId` | number | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `orderCreatedDate` | string | no |  |
| `deliveryDate` | string | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `pickedDate` | string | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `locationId` | number | no | Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `status` | string | no | When the status is omitted, NOT_SHIPPED is used as default. Use PENDING when you want to create sales order quotes. |
| `currency` | string | no | E.g. USD, EUR. All currently active currency codes in ISO 4217 format. Updatable only when sales order status is NOT_SHIPPED or PENDING. |
| `conversionRate` | number | no | Updatable only when sales order status is PACKED or DELIVERED, otherwise it will fail with 422. |
| `conversionDate` | string | no | Updatable only when sales order status is PACKED or DELIVERED, otherwise it will fail with 422. |
| `additionalInfo` | string | no |  |
| `customerRef` | string | no |  |
| `trackingNumber` | string | no |  |
| `trackingNumberUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalInfo": "string",
      "addresses": [
        {
          "city": "string",
          "company": "string",
          "country": "string",
          "createdAt": "string",
          "entityType": "string",
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "line1": "string",
          "line2": "string",
          "phone": "string",
          "salesOrderId": 1,
          "state": "string",
          "updatedAt": "string",
          "zip": "string"
        }
      ],
      "billingAddressId": 1,
      "conversionDate": "string",
      "conversionRate": 1,
      "createdAt": "string",
      "currency": "string",
      "customerId": 1,
      "customerRef": "string",
      "deletedAt": "string",
      "deliveryDate": "string",
      "ecommerceOrderId": "string",
      "ecommerceOrderType": "string",
      "ecommerceStoreName": "Ava Chen",
      "id": 1,
      "ingredientAvailability": "string",
      "invoicingStatus": "string",
      "linkedManufacturingOrderId": 1,
      "locationId": 1,
      "orderCreatedDate": "string",
      "orderNo": "string",
      "pickedDate": "string",
      "productAvailability": "string",
      "productionStatus": "string",
      "shippingAddressId": 1,
      "source": "string",
      "status": "string",
      "trackingNumber": "string",
      "trackingNumberUrl": "https://example.com",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInfo` | string |  |
| `addresses` | array<object> |  |
| `addresses[].city` | string |  |
| `addresses[].company` | string |  |
| `addresses[].country` | string |  |
| `addresses[].createdAt` | string |  |
| `addresses[].entityType` | string |  |
| `addresses[].firstName` | string |  |
| `addresses[].id` | number |  |
| `addresses[].lastName` | string |  |
| `addresses[].line1` | string |  |
| `addresses[].line2` | string |  |
| `addresses[].phone` | string |  |
| `addresses[].salesOrderId` | number |  |
| `addresses[].state` | string |  |
| `addresses[].updatedAt` | string |  |
| `addresses[].zip` | string |  |
| `billingAddressId` | number |  |
| `conversionDate` | string |  |
| `conversionRate` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customerId` | number |  |
| `customerRef` | string |  |
| `deletedAt` | string |  |
| `deliveryDate` | string |  |
| `ecommerceOrderId` | string |  |
| `ecommerceOrderType` | string |  |
| `ecommerceStoreName` | string |  |
| `id` | number |  |
| `ingredientAvailability` | string |  |
| `invoicingStatus` | string |  |
| `linkedManufacturingOrderId` | number |  |
| `locationId` | number |  |
| `orderCreatedDate` | string |  |
| `orderNo` | string |  |
| `pickedDate` | string |  |
| `productAvailability` | string |  |
| `productionStatus` | string |  |
| `shippingAddressId` | number |  |
| `source` | string |  |
| `status` | string |  |
| `trackingNumber` | string |  |
| `trackingNumberUrl` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `PATCH /sales_orders/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-order.md) for the provider-specific parameters and requirements.

