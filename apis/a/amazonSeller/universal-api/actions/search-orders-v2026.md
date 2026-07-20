# Amazon Seller: Search Orders

Finds orders in Amazon Seller by creation or update time.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/search-orders-v2026
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/search-orders-v2026?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/search-orders-v2026?${params}`, {
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
| `marketplaceIds` | list<string> | no | Find orders placed in only the marketplaces you select here. One of: `A13V1IB3VIYZZH`, `A17E79C6D8DWNP`, `A1805IZSGTT6HS`, `A19VAU5U5O7RUS`, `A1AM78C64UM0Y8`, `A1C3SOZRARQ6R3`, `A1F83G8C2ARO7P`, `A1PA6795UKMFR9`, `A1RKKUPIHCS9HS`, `A1VC38T7YXB528`, `A21TJRUUN4KGV`, `A28R8C7NBKEWEA`, `A2EUQ1WTGCTBG2`, `A2NODRKZP88ZB9`, `A2Q3Y263D00KWC`, `A2VIGQ35RCS4UG`, `A33AVAJ2PDY3EV`, `A39IBJ37TRP1C6`, `AE08WJ6YKNBMC`, `AMEN7PMS3EDWL`, `APJ6JRA9NG5V4`, `ARBP9OOSHTCHU`, `ATVPDKIKX0DER`. Accepts multiple values in one string. |
| `includedData` | list<string> | no | A list of datasets to include in the response. Accepts multiple values as an array. |
| `fulfilledBy` | list<string> | no | The response includes orders that are fulfilled by the parties that you choose. When nothing is selected all are returned. Accepts multiple values as an array. |
| `fulfillmentStatuses` | list<string> | no | Choose one or more statuses to filter the results. Accepts multiple values as an array. |
| `createdAfter` | date | no |  |
| `createdBefore` | string | no |  |
| `lastUpdatedAfter` | string | no |  |
| `lastUpdatedBefore` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyer": {
        "buyerEmail": "ava@example.com",
        "buyerName": "Ava Chen"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "fulfillment": {
        "deliverByWindow": {
          "earliestDateTime": "2026-05-07T12:00:00.000Z",
          "latestDateTime": "2026-05-07T12:00:00.000Z"
        },
        "fulfilledBy": "string",
        "fulfillmentServiceLevel": "string",
        "fulfillmentStatus": "string",
        "shipByWindow": {
          "earliestDateTime": "2026-05-07T12:00:00.000Z",
          "latestDateTime": "2026-05-07T12:00:00.000Z"
        }
      },
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "orderId": "string",
      "orderItems": [
        {
          "fulfillment": {
            "quantityFulfilled": 1,
            "quantityUnfulfilled": 1
          },
          "orderItemId": "string",
          "proceeds": {
            "breakdowns": [
              {
                "subtotal": {
                  "amount": "string",
                  "currencyCode": "string"
                },
                "type": "string"
              }
            ],
            "proceedsTotal": {
              "amount": "string",
              "currencyCode": "string"
            }
          },
          "product": {
            "asin": "string",
            "condition": {
              "conditionSubtype": "string",
              "conditionType": "string"
            },
            "price": {
              "unitPrice": {
                "amount": "string",
                "currencyCode": "string"
              }
            },
            "sellerSku": "string",
            "title": "string"
          },
          "quantityOrdered": 1
        }
      ],
      "packages": [
        {
          "carrier": "string",
          "createdTime": "string",
          "packageItems": [
            {
              "orderItemId": "string",
              "quantity": 1
            }
          ],
          "packageReferenceId": "string",
          "packageStatus": {
            "status": "string"
          },
          "shipFromAddress": {
            "addressLine1": "string",
            "city": "string",
            "countryCode": "string",
            "name": "Ava Chen",
            "postalCode": "string",
            "stateOrRegion": "string"
          },
          "shippingService": "string",
          "shipTime": "string",
          "trackingNumber": "string"
        }
      ],
      "proceeds": {
        "grandTotal": {
          "amount": "string",
          "currencyCode": "string"
        }
      },
      "programs": [
        "string"
      ],
      "recipient": {
        "deliveryAddress": {
          "addressLine1": "string",
          "addressType": "string",
          "city": "Ava Chen",
          "countryCode": "string",
          "name": "Ava Chen",
          "postalCode": "string",
          "stateOrRegion": "string"
        }
      },
      "salesChannel": {
        "channelName": "Ava Chen",
        "marketplaceId": "string",
        "marketplaceName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyer.buyerEmail` | string |  |
| `buyer.buyerName` | string |  |
| `createdTime` | date |  |
| `fulfillment.deliverByWindow.earliestDateTime` | date |  |
| `fulfillment.deliverByWindow.latestDateTime` | date |  |
| `fulfillment.fulfilledBy` | string |  |
| `fulfillment.fulfillmentServiceLevel` | string |  |
| `fulfillment.fulfillmentStatus` | string |  |
| `fulfillment.shipByWindow.earliestDateTime` | date |  |
| `fulfillment.shipByWindow.latestDateTime` | date |  |
| `lastUpdatedTime` | date |  |
| `orderId` | string |  |
| `orderItems[].fulfillment.quantityFulfilled` | number |  |
| `orderItems[].fulfillment.quantityUnfulfilled` | number |  |
| `orderItems[].orderItemId` | string |  |
| `orderItems[].proceeds.breakdowns[].subtotal.amount` | string |  |
| `orderItems[].proceeds.breakdowns[].subtotal.currencyCode` | string |  |
| `orderItems[].proceeds.breakdowns[].type` | string |  |
| `orderItems[].proceeds.proceedsTotal.amount` | string |  |
| `orderItems[].proceeds.proceedsTotal.currencyCode` | string |  |
| `orderItems[].product.asin` | string |  |
| `orderItems[].product.condition.conditionSubtype` | string |  |
| `orderItems[].product.condition.conditionType` | string |  |
| `orderItems[].product.price.unitPrice.amount` | string |  |
| `orderItems[].product.price.unitPrice.currencyCode` | string |  |
| `orderItems[].product.sellerSku` | string |  |
| `orderItems[].product.title` | string |  |
| `orderItems[].quantityOrdered` | number |  |
| `packages[].carrier` | string |  |
| `packages[].createdTime` | string |  |
| `packages[].packageItems[].orderItemId` | string |  |
| `packages[].packageItems[].quantity` | number |  |
| `packages[].packageReferenceId` | string |  |
| `packages[].packageStatus.status` | string |  |
| `packages[].shipFromAddress.addressLine1` | string |  |
| `packages[].shipFromAddress.city` | string |  |
| `packages[].shipFromAddress.countryCode` | string |  |
| `packages[].shipFromAddress.name` | string |  |
| `packages[].shipFromAddress.postalCode` | string |  |
| `packages[].shipFromAddress.stateOrRegion` | string |  |
| `packages[].shippingService` | string |  |
| `packages[].shipTime` | string |  |
| `packages[].trackingNumber` | string |  |
| `proceeds.grandTotal.amount` | string |  |
| `proceeds.grandTotal.currencyCode` | string |  |
| `programs[]` | string |  |
| `recipient.deliveryAddress.addressLine1` | string |  |
| `recipient.deliveryAddress.addressType` | string |  |
| `recipient.deliveryAddress.city` | string |  |
| `recipient.deliveryAddress.countryCode` | string |  |
| `recipient.deliveryAddress.name` | string |  |
| `recipient.deliveryAddress.postalCode` | string |  |
| `recipient.deliveryAddress.stateOrRegion` | string |  |
| `salesChannel.channelName` | string |  |
| `salesChannel.marketplaceId` | string |  |
| `salesChannel.marketplaceName` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET orders/2026-01-01/orders` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-orders-v2026.md) for the provider-specific parameters and requirements.

