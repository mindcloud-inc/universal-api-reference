# Katana: Retrieve Sales Order

Retrieves a sales order by ID from Katana.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-sales-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-sales-order?${params}`, {
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
| `id` | number | yes | Sales order id |

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
      "deliveryDate": "string",
      "ecommerceOrderId": "string",
      "ecommerceOrderType": "string",
      "ecommerceStoreName": "Ava Chen",
      "id": 1,
      "ingredientAvailability": "string",
      "ingredientExpectedDate": "string",
      "invoicingStatus": "string",
      "locationId": 1,
      "orderCreatedDate": "string",
      "orderNo": "string",
      "pickedDate": "string",
      "productAvailability": "string",
      "productExpectedDate": "string",
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
            {
              "batchId": 1,
              "quantity": 1
            }
          ],
          "conversionDate": "string",
          "conversionRate": 1,
          "createdAt": "string",
          "id": 1,
          "linkedManufacturingOrderId": 1,
          "locationId": 1,
          "pricePerUnit": 1,
          "pricePerUnitInBaseCurrency": 1,
          "productAvailability": "string",
          "productExpectedDate": "string",
          "quantity": 1,
          "salesOrderId": 1,
          "serialNumbers": [
            1
          ],
          "taxRateId": 1,
          "total": 1,
          "totalDiscount": "string",
          "totalInBaseCurrency": 1,
          "updatedAt": "string",
          "variantId": 1
        }
      ],
      "shippingAddressId": 1,
      "shippingFee": {
        "amount": "string",
        "description": "string",
        "id": 1,
        "salesOrderId": 1,
        "taxRateId": 1
      },
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
| `deliveryDate` | string |  |
| `ecommerceOrderId` | string |  |
| `ecommerceOrderType` | string |  |
| `ecommerceStoreName` | string |  |
| `id` | number |  |
| `ingredientAvailability` | string |  |
| `ingredientExpectedDate` | string |  |
| `invoicingStatus` | string |  |
| `locationId` | number |  |
| `orderCreatedDate` | string |  |
| `orderNo` | string |  |
| `pickedDate` | string |  |
| `productAvailability` | string |  |
| `productExpectedDate` | string |  |
| `productionStatus` | string |  |
| `salesOrderRows` | array<object> |  |
| `salesOrderRows[].attributes` | array<object> |  |
| `salesOrderRows[].attributes[].key` | string |  |
| `salesOrderRows[].attributes[].value` | string |  |
| `salesOrderRows[].batchTransactions` | array<object> |  |
| `salesOrderRows[].batchTransactions[].batchId` | number |  |
| `salesOrderRows[].batchTransactions[].quantity` | number |  |
| `salesOrderRows[].conversionDate` | string |  |
| `salesOrderRows[].conversionRate` | number |  |
| `salesOrderRows[].createdAt` | string |  |
| `salesOrderRows[].id` | number |  |
| `salesOrderRows[].linkedManufacturingOrderId` | number |  |
| `salesOrderRows[].locationId` | number |  |
| `salesOrderRows[].pricePerUnit` | number |  |
| `salesOrderRows[].pricePerUnitInBaseCurrency` | number |  |
| `salesOrderRows[].productAvailability` | string |  |
| `salesOrderRows[].productExpectedDate` | string |  |
| `salesOrderRows[].quantity` | number |  |
| `salesOrderRows[].salesOrderId` | number |  |
| `salesOrderRows[].serialNumbers` | array<number> |  |
| `salesOrderRows[].taxRateId` | number |  |
| `salesOrderRows[].total` | number |  |
| `salesOrderRows[].totalDiscount` | string |  |
| `salesOrderRows[].totalInBaseCurrency` | number |  |
| `salesOrderRows[].updatedAt` | string |  |
| `salesOrderRows[].variantId` | number |  |
| `shippingAddressId` | number |  |
| `shippingFee` | object |  |
| `shippingFee.amount` | string |  |
| `shippingFee.description` | string |  |
| `shippingFee.id` | number |  |
| `shippingFee.salesOrderId` | number |  |
| `shippingFee.taxRateId` | number |  |
| `source` | string |  |
| `status` | string |  |
| `total` | number |  |
| `totalInBaseCurrency` | number |  |
| `trackingNumber` | string |  |
| `trackingNumberUrl` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /sales_orders/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-sales-order.md) for the provider-specific parameters and requirements.

