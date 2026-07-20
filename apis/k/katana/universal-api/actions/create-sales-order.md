# Katana: Create Sales Order

Creates a new sales order in Katana.

```
POST https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderNo": "string",
  "customerId": 1,
  "salesOrderRows[]": [
    {}
  ],
  "salesOrderRows[].quantity": 1,
  "salesOrderRows[].variantId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/create-sales-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderNo": "string",
    "customerId": 1,
    "salesOrderRows[]": [{}],
    "salesOrderRows[].quantity": 1,
    "salesOrderRows[].variantId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderNo` | string | yes |  |
| `customerId` | number | yes |  |
| `salesOrderRows[]` | array<object> | yes |  |
| `salesOrderRows[].quantity` | number | yes |  |
| `salesOrderRows[].variantId` | number | yes |  |
| `salesOrderRows[].taxRateId` | number | no |  |
| `salesOrderRows[].locationId` | number | no |  |
| `salesOrderRows[].attributes[]` | array<object> | no |  |
| `salesOrderRows[].attributes[].key` | string | no |  |
| `salesOrderRows[].attributes[].value` | string | no |  |
| `salesOrderRows[].pricePerUnit` | number | no |  |
| `salesOrderRows[].totalDiscount` | number | no |  |
| `trackingNumber` | string | no |  |
| `trackingNumberUrl` | string | no |  |
| `addresses[]` | array<object> | no |  |
| `addresses[].entityType` | string | no |  |
| `addresses[].firstName` | string | no |  |
| `addresses[].lastName` | string | no |  |
| `addresses[].company` | string | no |  |
| `addresses[].phone` | string | no |  |
| `addresses[].line1` | string | no |  |
| `addresses[].line2` | string | no |  |
| `addresses[].city` | string | no |  |
| `addresses[].state` | string | no |  |
| `addresses[].zip` | string | no |  |
| `addresses[].country` | string | no |  |
| `orderCreatedDate` | string | no |  |
| `deliveryDate` | string | no |  |
| `currency` | string | no | E.g. USD, EUR. All currently active currency codes in ISO 4217 format. |
| `locationId` | number | no |  |
| `status` | string | no | When the status is omitted, NOT_SHIPPED is used as default. Use PENDING when you want to create sales order quotes. |
| `additionalInfo` | string | no |  |
| `customerRef` | string | no |  |
| `ecommerceOrderType` | string | no |  |
| `ecommerceStoreName` | string | no |  |
| `ecommerceOrderId` | string | no |  |

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
      "locationId": 1,
      "orderCreatedDate": "string",
      "orderNo": "string",
      "pickedDate": "string",
      "productAvailability": "string",
      "productionStatus": "string",
      "salesOrderRows": [
        {
          "attributes": [
            {
              "key": "string",
              "value": "string"
            }
          ],
          "batchTransactions": [
            "string"
          ],
          "conversionDate": "string",
          "conversionRate": "string",
          "createdAt": "string",
          "id": 1,
          "locationId": 1,
          "pricePerUnit": 1,
          "quantity": 1,
          "salesOrderId": 1,
          "taxRateId": 1,
          "total": 1,
          "totalInBaseCurrency": 1,
          "updatedAt": "string",
          "variantId": 1
        }
      ],
      "shippingAddressId": 1,
      "source": "string",
      "status": "string",
      "total": 1,
      "totalInBaseCurrency": 1,
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
| `locationId` | number |  |
| `orderCreatedDate` | string |  |
| `orderNo` | string |  |
| `pickedDate` | string |  |
| `productAvailability` | string |  |
| `productionStatus` | string |  |
| `salesOrderRows` | array<object> |  |
| `salesOrderRows[].attributes` | array<object> |  |
| `salesOrderRows[].attributes[].key` | string |  |
| `salesOrderRows[].attributes[].value` | string |  |
| `salesOrderRows[].batchTransactions` | array<string> |  |
| `salesOrderRows[].conversionDate` | string |  |
| `salesOrderRows[].conversionRate` | string |  |
| `salesOrderRows[].createdAt` | string |  |
| `salesOrderRows[].id` | number |  |
| `salesOrderRows[].locationId` | number |  |
| `salesOrderRows[].pricePerUnit` | number |  |
| `salesOrderRows[].quantity` | number |  |
| `salesOrderRows[].salesOrderId` | number |  |
| `salesOrderRows[].taxRateId` | number |  |
| `salesOrderRows[].total` | number |  |
| `salesOrderRows[].totalInBaseCurrency` | number |  |
| `salesOrderRows[].updatedAt` | string |  |
| `salesOrderRows[].variantId` | number |  |
| `shippingAddressId` | number |  |
| `source` | string |  |
| `status` | string |  |
| `total` | number |  |
| `totalInBaseCurrency` | number |  |
| `trackingNumber` | string |  |
| `trackingNumberUrl` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `POST /sales_orders` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-order.md) for the provider-specific parameters and requirements.

