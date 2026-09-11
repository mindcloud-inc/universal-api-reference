# BigCommerce (B2B): Get invoices



```
GET https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce (B2B) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-invoices?${params}`, {
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
| `offset` | string | no |  |
| `sortby` | string | no |  |
| `invoiceNumber` | string | no |  |
| `customername` | string | no |  |
| `customerid` | string | no |  |
| `status` | string | no |  |
| `begindateat` | date | no |  |
| `enddateat` | date | no |  |
| `externalid` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bcGroupName": "Ava Chen",
      "bcId": 1,
      "channelId": "string",
      "channelName": "Ava Chen",
      "createdAt": 1,
      "customerBcGroupName": {},
      "customerBcId": {},
      "customerId": "string",
      "customerName": "Ava Chen",
      "details": {
        "details": {
          "lineItems": [
            {
              "comments": "string",
              "description": "string",
              "productId": 1,
              "quantity": 1,
              "sku": "string",
              "type": "string",
              "unitDiscount": {
                "code": "string",
                "value": 1
              },
              "unitPrice": {
                "code": "string",
                "value": "string"
              }
            }
          ]
        },
        "header": {
          "billingAddress": {
            "city": "string",
            "country": "string",
            "firstName": "Ava",
            "lastName": "Chen",
            "state": "string",
            "street1": "string",
            "street2": "string",
            "zipCode": "string"
          },
          "costLines": [
            {
              "amount": {
                "code": "string",
                "value": "string"
              },
              "description": "string"
            }
          ],
          "orderDate": 1
        },
        "type": "string"
      },
      "dueDate": 1,
      "externalCustomerId": {},
      "externalId": {},
      "externalPdfUrl": {},
      "id": 1,
      "invoiceNumber": "string",
      "notAllowedPay": 1,
      "openBalance": {
        "code": "string",
        "value": "string"
      },
      "orderNumber": 1,
      "originalBalance": {
        "code": "string",
        "value": "string"
      },
      "pendingPaymentCount": 1,
      "purchaseOrderNumber": {},
      "source": 1,
      "status": 1,
      "storeHash": "string",
      "termsConditions": "string",
      "type": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bcGroupName` | string |  |
| `bcId` | number |  |
| `channelId` | string |  |
| `channelName` | string |  |
| `createdAt` | number |  |
| `customerBcGroupName` | object |  |
| `customerBcId` | object |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `details.details.lineItems[].comments` | string |  |
| `details.details.lineItems[].description` | string |  |
| `details.details.lineItems[].productId` | number |  |
| `details.details.lineItems[].quantity` | number |  |
| `details.details.lineItems[].sku` | string |  |
| `details.details.lineItems[].type` | string |  |
| `details.details.lineItems[].unitDiscount.code` | string |  |
| `details.details.lineItems[].unitDiscount.value` | number |  |
| `details.details.lineItems[].unitPrice.code` | string |  |
| `details.details.lineItems[].unitPrice.value` | string |  |
| `details.header.billingAddress.city` | string |  |
| `details.header.billingAddress.country` | string |  |
| `details.header.billingAddress.firstName` | string |  |
| `details.header.billingAddress.lastName` | string |  |
| `details.header.billingAddress.state` | string |  |
| `details.header.billingAddress.street1` | string |  |
| `details.header.billingAddress.street2` | string |  |
| `details.header.billingAddress.zipCode` | string |  |
| `details.header.costLines[].amount.code` | string |  |
| `details.header.costLines[].amount.value` | string |  |
| `details.header.costLines[].description` | string |  |
| `details.header.orderDate` | number |  |
| `details.type` | string |  |
| `dueDate` | number |  |
| `externalCustomerId` | object |  |
| `externalId` | object |  |
| `externalPdfUrl` | object |  |
| `id` | number |  |
| `invoiceNumber` | string |  |
| `notAllowedPay` | number |  |
| `openBalance.code` | string |  |
| `openBalance.value` | string |  |
| `orderNumber` | number |  |
| `originalBalance.code` | string |  |
| `originalBalance.value` | string |  |
| `pendingPaymentCount` | number |  |
| `purchaseOrderNumber` | object |  |
| `source` | number |  |
| `status` | number |  |
| `storeHash` | string |  |
| `termsConditions` | string |  |
| `type` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native BigCommerce (B2B) API, this operation is `GET ip/invoices` (base URL `https://api-b2b.bigcommerce.com/api/v3/io/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoices.md) for the provider-specific parameters and requirements.

