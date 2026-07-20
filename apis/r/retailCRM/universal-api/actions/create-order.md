# retailCRM: Create Order

Creates a new order in retailCRM.

```
POST https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site": "string",
  "order.externalId": "string",
  "order.firstName": "Ava",
  "order.phone": "string",
  "order.orderType": "string",
  "order.orderMethod": "string",
  "order.items[0].productName": "Ava Chen",
  "order.items[0].quantity": 1,
  "order.items[0].initialPrice": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site": "string",
    "order.externalId": "string",
    "order.firstName": "Ava",
    "order.phone": "string",
    "order.orderType": "string",
    "order.orderMethod": "string",
    "order.items[0].productName": "Ava Chen",
    "order.items[0].quantity": 1,
    "order.items[0].initialPrice": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `site` | list | yes |  |
| `order.externalId` | string | yes |  |
| `order.firstName` | string | yes |  |
| `order.lastName` | string | no |  |
| `order.phone` | string | yes |  |
| `order.orderType` | list | yes |  |
| `order.orderMethod` | list | yes |  |
| `order.items[0].productName` | string | yes |  |
| `order.items[0].quantity` | number | yes |  |
| `order.items[0].initialPrice` | number | yes |  |
| `order.items[0].purchasePrice` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "order": {
        "bonusesChargeTotal": 1,
        "bonusesCreditTotal": 1,
        "call": true,
        "contact": {
          "averageSumm": 1,
          "bad": true,
          "contragent": {
            "contragentType": "string"
          },
          "createdAt": "string",
          "customerSubscriptions": [
            {
              "subscribed": true,
              "subscription": {
                "active": true,
                "autoSubscribe": true,
                "channel": "string",
                "code": "string",
                "id": 1,
                "name": "Ava Chen",
                "ordering": 1
              }
            }
          ],
          "customFields": [
            "string"
          ],
          "firstName": "Ava",
          "id": 1,
          "isContact": true,
          "lastName": "Chen",
          "marginSumm": 1,
          "mgCustomers": [
            "string"
          ],
          "ordersCount": 1,
          "personalDiscount": 1,
          "phones": [
            {
              "number": "string"
            }
          ],
          "segments": [
            "string"
          ],
          "site": "string",
          "tags": [
            "string"
          ],
          "totalSumm": 1,
          "type": "string",
          "vip": true
        },
        "contragent": {
          "contragentType": "string"
        },
        "countryIso": "string",
        "createdAt": "string",
        "currency": "string",
        "customer": {
          "averageSumm": 1,
          "bad": true,
          "contragent": {
            "contragentType": "string"
          },
          "createdAt": "string",
          "customerSubscriptions": [
            "string"
          ],
          "customFields": [
            "string"
          ],
          "firstName": "Ava",
          "id": 1,
          "isContact": true,
          "lastName": "Chen",
          "marginSumm": 1,
          "mgCustomers": [
            "string"
          ],
          "ordersCount": 1,
          "personalDiscount": 1,
          "phones": [
            {
              "number": "string"
            }
          ],
          "segments": [
            "string"
          ],
          "site": "string",
          "tags": [
            "string"
          ],
          "totalSumm": 1,
          "type": "string",
          "vip": true
        },
        "customFields": [
          "string"
        ],
        "delivery": {
          "address": {},
          "cost": 1,
          "netCost": 1
        },
        "expired": true,
        "externalId": "string",
        "firstName": "Ava",
        "fromApi": true,
        "id": 1,
        "items": [
          {
            "bonusesChargeTotal": 1,
            "bonusesCreditTotal": 1,
            "createdAt": "string",
            "discounts": [
              "string"
            ],
            "discountTotal": 1,
            "id": 1,
            "initialPrice": 1,
            "markingObjects": [
              "string"
            ],
            "offer": {
              "displayName": "Ava Chen",
              "id": 1,
              "name": "Ava Chen",
              "quantity": 1,
              "unit": {
                "code": "string",
                "name": "Ava Chen",
                "sym": "string"
              },
              "xmlId": "string"
            },
            "ordering": 1,
            "prices": [
              {
                "price": 1,
                "quantity": 1
              }
            ],
            "properties": [
              "string"
            ],
            "purchasePrice": 1,
            "quantity": 1,
            "status": "string"
          }
        ],
        "lastName": "Chen",
        "links": [
          "https://example.com"
        ],
        "markDatetime": "string",
        "number": "string",
        "orderMethod": "string",
        "orderType": "string",
        "payments": [
          "string"
        ],
        "phone": "string",
        "prepaySum": 1,
        "privilegeType": "string",
        "purchaseSumm": 1,
        "shipped": true,
        "site": "string",
        "slug": 1,
        "status": "string",
        "statusUpdatedAt": "string",
        "summ": 1,
        "totalSumm": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `order.bonusesChargeTotal` | number |  |
| `order.bonusesCreditTotal` | number |  |
| `order.call` | boolean |  |
| `order.contact.averageSumm` | number |  |
| `order.contact.bad` | boolean |  |
| `order.contact.contragent.contragentType` | string |  |
| `order.contact.createdAt` | string |  |
| `order.contact.customerSubscriptions[].subscribed` | boolean |  |
| `order.contact.customerSubscriptions[].subscription.active` | boolean |  |
| `order.contact.customerSubscriptions[].subscription.autoSubscribe` | boolean |  |
| `order.contact.customerSubscriptions[].subscription.channel` | string |  |
| `order.contact.customerSubscriptions[].subscription.code` | string |  |
| `order.contact.customerSubscriptions[].subscription.id` | number |  |
| `order.contact.customerSubscriptions[].subscription.name` | string |  |
| `order.contact.customerSubscriptions[].subscription.ordering` | number |  |
| `order.contact.customFields` | array |  |
| `order.contact.firstName` | string |  |
| `order.contact.id` | number |  |
| `order.contact.isContact` | boolean |  |
| `order.contact.lastName` | string |  |
| `order.contact.marginSumm` | number |  |
| `order.contact.mgCustomers` | array |  |
| `order.contact.ordersCount` | number |  |
| `order.contact.personalDiscount` | number |  |
| `order.contact.phones[].number` | string |  |
| `order.contact.segments` | array |  |
| `order.contact.site` | string |  |
| `order.contact.tags` | array |  |
| `order.contact.totalSumm` | number |  |
| `order.contact.type` | string |  |
| `order.contact.vip` | boolean |  |
| `order.contragent.contragentType` | string |  |
| `order.countryIso` | string |  |
| `order.createdAt` | string |  |
| `order.currency` | string |  |
| `order.customer.averageSumm` | number |  |
| `order.customer.bad` | boolean |  |
| `order.customer.contragent.contragentType` | string |  |
| `order.customer.createdAt` | string |  |
| `order.customer.customerSubscriptions` | array |  |
| `order.customer.customFields` | array |  |
| `order.customer.firstName` | string |  |
| `order.customer.id` | number |  |
| `order.customer.isContact` | boolean |  |
| `order.customer.lastName` | string |  |
| `order.customer.marginSumm` | number |  |
| `order.customer.mgCustomers` | array |  |
| `order.customer.ordersCount` | number |  |
| `order.customer.personalDiscount` | number |  |
| `order.customer.phones[].number` | string |  |
| `order.customer.segments` | array |  |
| `order.customer.site` | string |  |
| `order.customer.tags` | array |  |
| `order.customer.totalSumm` | number |  |
| `order.customer.type` | string |  |
| `order.customer.vip` | boolean |  |
| `order.customFields` | array |  |
| `order.delivery.address` | object |  |
| `order.delivery.cost` | number |  |
| `order.delivery.netCost` | number |  |
| `order.expired` | boolean |  |
| `order.externalId` | string |  |
| `order.firstName` | string |  |
| `order.fromApi` | boolean |  |
| `order.id` | number |  |
| `order.items[].bonusesChargeTotal` | number |  |
| `order.items[].bonusesCreditTotal` | number |  |
| `order.items[].createdAt` | string |  |
| `order.items[].discounts` | array |  |
| `order.items[].discountTotal` | number |  |
| `order.items[].id` | number |  |
| `order.items[].initialPrice` | number |  |
| `order.items[].markingObjects` | array |  |
| `order.items[].offer.displayName` | string |  |
| `order.items[].offer.id` | number |  |
| `order.items[].offer.name` | string |  |
| `order.items[].offer.quantity` | number |  |
| `order.items[].offer.unit.code` | string |  |
| `order.items[].offer.unit.name` | string |  |
| `order.items[].offer.unit.sym` | string |  |
| `order.items[].offer.xmlId` | string |  |
| `order.items[].ordering` | number |  |
| `order.items[].prices[].price` | number |  |
| `order.items[].prices[].quantity` | number |  |
| `order.items[].properties` | array |  |
| `order.items[].purchasePrice` | number |  |
| `order.items[].quantity` | number |  |
| `order.items[].status` | string |  |
| `order.lastName` | string |  |
| `order.links` | array |  |
| `order.markDatetime` | string |  |
| `order.number` | string |  |
| `order.orderMethod` | string |  |
| `order.orderType` | string |  |
| `order.payments` | array |  |
| `order.phone` | string |  |
| `order.prepaySum` | number |  |
| `order.privilegeType` | string |  |
| `order.purchaseSumm` | number |  |
| `order.shipped` | boolean |  |
| `order.site` | string |  |
| `order.slug` | number |  |
| `order.status` | string |  |
| `order.statusUpdatedAt` | string |  |
| `order.summ` | number |  |
| `order.totalSumm` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native retailCRM API, this operation is `POST /orders/create` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

