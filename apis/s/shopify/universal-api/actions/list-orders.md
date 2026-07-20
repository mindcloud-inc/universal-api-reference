# Shopify: List Orders

Retrieves orders from Shopify with GraphQL.

```
GET https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopify/latest/actions/list-orders?${params}`, {
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
| `createdAt` | string | no | Date created after |
| `updatedAt` | string | no | Date updated after |
| `updatedBefore` | string | no |  |
| `financialStatus` | list | no |  |
| `fulfillmentStatus` | list<string> | no |  |
| `email` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids[]` | array<string> | no |  |
| `names[]` | array<string> | no |  |
| `customQuery` | string | no | Optional Shopify order search query to combine with the built-in filters. |
| `reverse` | boolean | no | Reverse the sort order of the results |
| `simple` | boolean | no | Return a lighter order payload when you only need core order fields. Leave OFF if you need only specific advanced fields |
| `purchasingEntity` | boolean | no | Adds field: purchasingEntity |
| `totalPriceSet` | boolean | no | Adds field: totalPriceSet |
| `currentCartDiscountAmountSet` | boolean | no | Adds field: currentCartDiscountAmountSet |
| `currentTotalDiscountsSet` | boolean | no | Adds field: currentTotalDiscountsSet |
| `currentTotalTaxSet` | boolean | no | Adds field: currentTotalTaxSet |
| `totalTaxSet` | boolean | no | Adds field: totalTaxSet |
| `currentTaxLines` | boolean | no | Adds field: currentTaxLines |
| `taxLine` | boolean | no | Adds field: taxLine |
| `fulfillmentOrders` | boolean | no | Adds field: fulfillmentOrders |
| `totalShippingPriceSet` | boolean | no | Adds field: totalShippingPriceSet |
| `shippingLine` | boolean | no | Adds field: shippingLine |
| `shippingLines` | boolean | no | Adds field: shippingLines |
| `billingAddress` | boolean | no | Adds field: billingAddress |
| `netPaymentSet` | boolean | no | Adds field: netPaymentSet |
| `customer` | boolean | no | Adds field: customer |
| `paymentGatewayNames` | boolean | no | Adds field: paymentGatewayNames |
| `retailLocation` | boolean | no | Adds field: retailLocation |
| `transactions` | boolean | no | Adds field: transactions |
| `metafields` | boolean | no | Adds field: metafields |
| `test` | boolean | no | Adds field: test |
| `advancedLineItems` | boolean | no | Adds metafields to Line Items |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {},
      "cancelledAt": {},
      "cancelReason": {},
      "closed": true,
      "closedAt": "string",
      "createdAt": "string",
      "currentCartDiscountAmountSet": {
        "presentmentMoney": {
          "amount": "string",
          "currencyCode": "string"
        },
        "shopMoney": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "currentTotalDiscountsSet": {
        "presentmentMoney": {
          "amount": "string",
          "currencyCode": "string"
        },
        "shopMoney": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "currentTotalTaxSet": {
        "presentmentMoney": {
          "amount": "string",
          "currencyCode": "string"
        },
        "shopMoney": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "customer": {
        "email": "ava@example.com",
        "firstName": {},
        "id": "string",
        "lastName": {},
        "legacyResourceId": "string",
        "phone": {}
      },
      "displayFinancialStatus": "string",
      "displayFulfillmentStatus": "string",
      "email": "ava@example.com",
      "fulfillmentOrders": [
        {
          "assignedLocation": {
            "location": {
              "id": "string",
              "legacyResourceId": "string",
              "name": "Ava Chen"
            },
            "name": "Ava Chen"
          },
          "createdAt": "string",
          "destination": {
            "address1": "string",
            "address2": {},
            "city": "string",
            "company": "string",
            "countryCode": "string",
            "firstName": {},
            "lastName": "Chen",
            "location": {},
            "province": "string",
            "zip": "string"
          },
          "id": "string",
          "lineItems": [
            {
              "id": "string",
              "inventoryItemId": "string",
              "lineItem": {
                "id": "string",
                "name": "Ava Chen",
                "quantity": 1,
                "sku": "string"
              }
            }
          ],
          "status": "string"
        }
      ],
      "id": "string",
      "legacyResourceId": "string",
      "lineItems": [
        {
          "currentQuantity": 1,
          "customAttributes": [
            {
              "key": "string",
              "value": "string"
            }
          ],
          "discountedTotalSet": {
            "presentmentMoney": {
              "amount": "string",
              "currencyCode": "string"
            },
            "shopMoney": {
              "amount": "string",
              "currencyCode": "string"
            }
          },
          "discountedUnitPriceSet": {
            "presentmentMoney": {
              "amount": "string",
              "currencyCode": "string"
            },
            "shopMoney": {
              "amount": "string",
              "currencyCode": "string"
            }
          },
          "id": "string",
          "isGiftCard": true,
          "name": "Ava Chen",
          "originalTotalSet": {
            "presentmentMoney": {
              "amount": "string",
              "currencyCode": "string"
            },
            "shopMoney": {
              "amount": "string",
              "currencyCode": "string"
            }
          },
          "originalUnitPriceSet": {
            "presentmentMoney": {
              "amount": "string",
              "currencyCode": "string"
            },
            "shopMoney": {
              "amount": "string",
              "currencyCode": "string"
            }
          },
          "product": {
            "handle": "string",
            "id": "string",
            "title": "string",
            "vendor": "string"
          },
          "quantity": 1,
          "requiresShipping": true,
          "sellingPlan": {},
          "sku": "string",
          "taxable": true,
          "title": "string",
          "unfulfilledQuantity": 1,
          "variant": {
            "id": "string",
            "legacyResourceId": "string",
            "price": "string",
            "sku": "string",
            "title": "string"
          },
          "variantTitle": {},
          "vendor": "string"
        }
      ],
      "name": "Ava Chen",
      "netPaymentSet": {
        "presentmentMoney": {
          "amount": "string",
          "currencyCode": "string"
        },
        "shopMoney": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "note": {},
      "paymentGatewayNames": [
        "Ava Chen"
      ],
      "processedAt": "string",
      "purchasingEntity": {
        "company": {
          "id": "string",
          "name": "Ava Chen"
        },
        "location": {
          "id": "string",
          "name": "Ava Chen"
        },
        "Typename": "Ava Chen"
      },
      "retailLocation": {},
      "shippingAddress": {
        "address1": "string",
        "address2": {},
        "city": "string",
        "company": "string",
        "countryCode": "string",
        "countryCodeV2": "string",
        "firstName": {},
        "lastName": "Chen",
        "phone": {},
        "province": "string",
        "provinceCode": "string",
        "zip": "string"
      },
      "shippingLine": {
        "carrierIdentifier": "string",
        "code": "string",
        "currentDiscountedPriceSet": {
          "presentmentMoney": {
            "amount": "string",
            "currencyCode": "string"
          },
          "shopMoney": {
            "amount": "string",
            "currencyCode": "string"
          }
        },
        "deliveryCategory": {},
        "title": "string"
      },
      "shippingLines": [
        {
          "carrierIdentifier": "string",
          "code": "string",
          "currentDiscountedPriceSet": {
            "presentmentMoney": {
              "amount": "string",
              "currencyCode": "string"
            },
            "shopMoney": {
              "amount": "string",
              "currencyCode": "string"
            }
          },
          "deliveryCategory": {}
        }
      ],
      "sourceIdentifier": {},
      "sourceName": "Ava Chen",
      "tags": [
        "string"
      ],
      "test": true,
      "totalPriceSet": {
        "presentmentMoney": {
          "amount": "string",
          "currencyCode": "string"
        },
        "shopMoney": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "totalShippingPriceSet": {
        "presentmentMoney": {
          "amount": "string",
          "currencyCode": "string"
        },
        "shopMoney": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "totalTaxSet": {
        "presentmentMoney": {
          "amount": "string",
          "currencyCode": "string"
        },
        "shopMoney": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "transactions": [
        {
          "amountSet": {
            "presentmentMoney": {
              "amount": "string",
              "currencyCode": "string"
            },
            "shopMoney": {
              "amount": "string",
              "currencyCode": "string"
            }
          },
          "authorizationCode": {},
          "authorizationExpiresAt": {},
          "createdAt": "string",
          "errorCode": {},
          "formattedGateway": "string",
          "gateway": "string",
          "id": "string",
          "kind": "string",
          "paymentDetails": {},
          "paymentId": "string",
          "processedAt": "string",
          "receiptJson": "string",
          "settlementCurrency": {},
          "settlementCurrencyRate": {},
          "status": "string",
          "test": true
        }
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress` | object |  |
| `cancelledAt` | object |  |
| `cancelReason` | object |  |
| `closed` | boolean |  |
| `closedAt` | string |  |
| `createdAt` | string |  |
| `currentCartDiscountAmountSet.presentmentMoney.amount` | string |  |
| `currentCartDiscountAmountSet.presentmentMoney.currencyCode` | string |  |
| `currentCartDiscountAmountSet.shopMoney.amount` | string |  |
| `currentCartDiscountAmountSet.shopMoney.currencyCode` | string |  |
| `currentTotalDiscountsSet.presentmentMoney.amount` | string |  |
| `currentTotalDiscountsSet.presentmentMoney.currencyCode` | string |  |
| `currentTotalDiscountsSet.shopMoney.amount` | string |  |
| `currentTotalDiscountsSet.shopMoney.currencyCode` | string |  |
| `currentTotalTaxSet.presentmentMoney.amount` | string |  |
| `currentTotalTaxSet.presentmentMoney.currencyCode` | string |  |
| `currentTotalTaxSet.shopMoney.amount` | string |  |
| `currentTotalTaxSet.shopMoney.currencyCode` | string |  |
| `customer.email` | string |  |
| `customer.firstName` | object |  |
| `customer.id` | string |  |
| `customer.lastName` | object |  |
| `customer.legacyResourceId` | string |  |
| `customer.phone` | object |  |
| `displayFinancialStatus` | string |  |
| `displayFulfillmentStatus` | string |  |
| `email` | string |  |
| `fulfillmentOrders[].assignedLocation.location.id` | string |  |
| `fulfillmentOrders[].assignedLocation.location.legacyResourceId` | string |  |
| `fulfillmentOrders[].assignedLocation.location.name` | string |  |
| `fulfillmentOrders[].assignedLocation.name` | string |  |
| `fulfillmentOrders[].createdAt` | string |  |
| `fulfillmentOrders[].destination.address1` | string |  |
| `fulfillmentOrders[].destination.address2` | object |  |
| `fulfillmentOrders[].destination.city` | string |  |
| `fulfillmentOrders[].destination.company` | string |  |
| `fulfillmentOrders[].destination.countryCode` | string |  |
| `fulfillmentOrders[].destination.firstName` | object |  |
| `fulfillmentOrders[].destination.lastName` | string |  |
| `fulfillmentOrders[].destination.location` | object |  |
| `fulfillmentOrders[].destination.province` | string |  |
| `fulfillmentOrders[].destination.zip` | string |  |
| `fulfillmentOrders[].id` | string |  |
| `fulfillmentOrders[].lineItems[].id` | string |  |
| `fulfillmentOrders[].lineItems[].inventoryItemId` | string |  |
| `fulfillmentOrders[].lineItems[].lineItem.id` | string |  |
| `fulfillmentOrders[].lineItems[].lineItem.name` | string |  |
| `fulfillmentOrders[].lineItems[].lineItem.quantity` | number |  |
| `fulfillmentOrders[].lineItems[].lineItem.sku` | string |  |
| `fulfillmentOrders[].status` | string |  |
| `id` | string |  |
| `legacyResourceId` | string |  |
| `lineItems[].currentQuantity` | number |  |
| `lineItems[].customAttributes[].key` | string |  |
| `lineItems[].customAttributes[].value` | string |  |
| `lineItems[].discountedTotalSet.presentmentMoney.amount` | string |  |
| `lineItems[].discountedTotalSet.presentmentMoney.currencyCode` | string |  |
| `lineItems[].discountedTotalSet.shopMoney.amount` | string |  |
| `lineItems[].discountedTotalSet.shopMoney.currencyCode` | string |  |
| `lineItems[].discountedUnitPriceSet.presentmentMoney.amount` | string |  |
| `lineItems[].discountedUnitPriceSet.presentmentMoney.currencyCode` | string |  |
| `lineItems[].discountedUnitPriceSet.shopMoney.amount` | string |  |
| `lineItems[].discountedUnitPriceSet.shopMoney.currencyCode` | string |  |
| `lineItems[].id` | string |  |
| `lineItems[].isGiftCard` | boolean |  |
| `lineItems[].name` | string |  |
| `lineItems[].originalTotalSet.presentmentMoney.amount` | string |  |
| `lineItems[].originalTotalSet.presentmentMoney.currencyCode` | string |  |
| `lineItems[].originalTotalSet.shopMoney.amount` | string |  |
| `lineItems[].originalTotalSet.shopMoney.currencyCode` | string |  |
| `lineItems[].originalUnitPriceSet.presentmentMoney.amount` | string |  |
| `lineItems[].originalUnitPriceSet.presentmentMoney.currencyCode` | string |  |
| `lineItems[].originalUnitPriceSet.shopMoney.amount` | string |  |
| `lineItems[].originalUnitPriceSet.shopMoney.currencyCode` | string |  |
| `lineItems[].product.handle` | string |  |
| `lineItems[].product.id` | string |  |
| `lineItems[].product.title` | string |  |
| `lineItems[].product.vendor` | string |  |
| `lineItems[].quantity` | number |  |
| `lineItems[].requiresShipping` | boolean |  |
| `lineItems[].sellingPlan` | object |  |
| `lineItems[].sku` | string |  |
| `lineItems[].taxable` | boolean |  |
| `lineItems[].title` | string |  |
| `lineItems[].unfulfilledQuantity` | number |  |
| `lineItems[].variant.id` | string |  |
| `lineItems[].variant.legacyResourceId` | string |  |
| `lineItems[].variant.price` | string |  |
| `lineItems[].variant.sku` | string |  |
| `lineItems[].variant.title` | string |  |
| `lineItems[].variantTitle` | object |  |
| `lineItems[].vendor` | string |  |
| `name` | string |  |
| `netPaymentSet.presentmentMoney.amount` | string |  |
| `netPaymentSet.presentmentMoney.currencyCode` | string |  |
| `netPaymentSet.shopMoney.amount` | string |  |
| `netPaymentSet.shopMoney.currencyCode` | string |  |
| `note` | object |  |
| `paymentGatewayNames[]` | string |  |
| `processedAt` | string |  |
| `purchasingEntity.company.id` | string |  |
| `purchasingEntity.company.name` | string |  |
| `purchasingEntity.location.id` | string |  |
| `purchasingEntity.location.name` | string |  |
| `purchasingEntity.Typename` | string |  |
| `retailLocation` | object |  |
| `shippingAddress.address1` | string |  |
| `shippingAddress.address2` | object |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.company` | string |  |
| `shippingAddress.countryCode` | string |  |
| `shippingAddress.countryCodeV2` | string |  |
| `shippingAddress.firstName` | object |  |
| `shippingAddress.lastName` | string |  |
| `shippingAddress.phone` | object |  |
| `shippingAddress.province` | string |  |
| `shippingAddress.provinceCode` | string |  |
| `shippingAddress.zip` | string |  |
| `shippingLine.carrierIdentifier` | string |  |
| `shippingLine.code` | string |  |
| `shippingLine.currentDiscountedPriceSet.presentmentMoney.amount` | string |  |
| `shippingLine.currentDiscountedPriceSet.presentmentMoney.currencyCode` | string |  |
| `shippingLine.currentDiscountedPriceSet.shopMoney.amount` | string |  |
| `shippingLine.currentDiscountedPriceSet.shopMoney.currencyCode` | string |  |
| `shippingLine.deliveryCategory` | object |  |
| `shippingLine.title` | string |  |
| `shippingLines[].carrierIdentifier` | string |  |
| `shippingLines[].code` | string |  |
| `shippingLines[].currentDiscountedPriceSet.presentmentMoney.amount` | string |  |
| `shippingLines[].currentDiscountedPriceSet.presentmentMoney.currencyCode` | string |  |
| `shippingLines[].currentDiscountedPriceSet.shopMoney.amount` | string |  |
| `shippingLines[].currentDiscountedPriceSet.shopMoney.currencyCode` | string |  |
| `shippingLines[].deliveryCategory` | object |  |
| `sourceIdentifier` | object |  |
| `sourceName` | string |  |
| `tags[]` | string |  |
| `test` | boolean |  |
| `totalPriceSet.presentmentMoney.amount` | string |  |
| `totalPriceSet.presentmentMoney.currencyCode` | string |  |
| `totalPriceSet.shopMoney.amount` | string |  |
| `totalPriceSet.shopMoney.currencyCode` | string |  |
| `totalShippingPriceSet.presentmentMoney.amount` | string |  |
| `totalShippingPriceSet.presentmentMoney.currencyCode` | string |  |
| `totalShippingPriceSet.shopMoney.amount` | string |  |
| `totalShippingPriceSet.shopMoney.currencyCode` | string |  |
| `totalTaxSet.presentmentMoney.amount` | string |  |
| `totalTaxSet.presentmentMoney.currencyCode` | string |  |
| `totalTaxSet.shopMoney.amount` | string |  |
| `totalTaxSet.shopMoney.currencyCode` | string |  |
| `transactions[].amountSet.presentmentMoney.amount` | string |  |
| `transactions[].amountSet.presentmentMoney.currencyCode` | string |  |
| `transactions[].amountSet.shopMoney.amount` | string |  |
| `transactions[].amountSet.shopMoney.currencyCode` | string |  |
| `transactions[].authorizationCode` | object |  |
| `transactions[].authorizationExpiresAt` | object |  |
| `transactions[].createdAt` | string |  |
| `transactions[].errorCode` | object |  |
| `transactions[].formattedGateway` | string |  |
| `transactions[].gateway` | string |  |
| `transactions[].id` | string |  |
| `transactions[].kind` | string |  |
| `transactions[].paymentDetails` | object |  |
| `transactions[].paymentId` | string |  |
| `transactions[].processedAt` | string |  |
| `transactions[].receiptJson` | string |  |
| `transactions[].settlementCurrency` | object |  |
| `transactions[].settlementCurrencyRate` | object |  |
| `transactions[].status` | string |  |
| `transactions[].test` | boolean |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Shopify API, this operation is `POST 2025-01/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

