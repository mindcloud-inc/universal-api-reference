# retailCRM: Get Order

Retrieves an order from retailCRM by external ID.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-order?connectionId=$CONNECTION_ID&externalId=string&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "externalId": "string",
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-order?${params}`, {
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
| `externalId` | string | yes |  |
| `by` | list | no | One of: `externalId`, `id`. Default: `externalId`. |
| `site` | list | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
        "managerId": 1,
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
        "managerId": 1,
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
        "address": {
          "countryIso": "string"
        },
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
      "managerComment": "string",
      "managerId": 1,
      "markDatetime": "string",
      "number": "string",
      "orderMethod": "string",
      "orderType": "string",
      "payments": {},
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bonusesChargeTotal` | number |  |
| `bonusesCreditTotal` | number |  |
| `call` | boolean |  |
| `contact.averageSumm` | number |  |
| `contact.bad` | boolean |  |
| `contact.contragent.contragentType` | string |  |
| `contact.createdAt` | string |  |
| `contact.customerSubscriptions[].subscribed` | boolean |  |
| `contact.customerSubscriptions[].subscription.active` | boolean |  |
| `contact.customerSubscriptions[].subscription.autoSubscribe` | boolean |  |
| `contact.customerSubscriptions[].subscription.channel` | string |  |
| `contact.customerSubscriptions[].subscription.code` | string |  |
| `contact.customerSubscriptions[].subscription.id` | number |  |
| `contact.customerSubscriptions[].subscription.name` | string |  |
| `contact.customerSubscriptions[].subscription.ordering` | number |  |
| `contact.customFields` | array |  |
| `contact.firstName` | string |  |
| `contact.id` | number |  |
| `contact.isContact` | boolean |  |
| `contact.lastName` | string |  |
| `contact.managerId` | number |  |
| `contact.marginSumm` | number |  |
| `contact.mgCustomers` | array |  |
| `contact.ordersCount` | number |  |
| `contact.personalDiscount` | number |  |
| `contact.phones[].number` | string |  |
| `contact.segments` | array |  |
| `contact.site` | string |  |
| `contact.tags` | array |  |
| `contact.totalSumm` | number |  |
| `contact.type` | string |  |
| `contact.vip` | boolean |  |
| `contragent.contragentType` | string |  |
| `countryIso` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `customer.averageSumm` | number |  |
| `customer.bad` | boolean |  |
| `customer.contragent.contragentType` | string |  |
| `customer.createdAt` | string |  |
| `customer.customerSubscriptions` | array |  |
| `customer.customFields` | array |  |
| `customer.firstName` | string |  |
| `customer.id` | number |  |
| `customer.isContact` | boolean |  |
| `customer.lastName` | string |  |
| `customer.managerId` | number |  |
| `customer.marginSumm` | number |  |
| `customer.mgCustomers` | array |  |
| `customer.ordersCount` | number |  |
| `customer.personalDiscount` | number |  |
| `customer.phones[].number` | string |  |
| `customer.segments` | array |  |
| `customer.site` | string |  |
| `customer.tags` | array |  |
| `customer.totalSumm` | number |  |
| `customer.type` | string |  |
| `customer.vip` | boolean |  |
| `customFields` | array |  |
| `delivery.address.countryIso` | string |  |
| `delivery.cost` | number |  |
| `delivery.netCost` | number |  |
| `expired` | boolean |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `fromApi` | boolean |  |
| `id` | number |  |
| `items[].bonusesChargeTotal` | number |  |
| `items[].bonusesCreditTotal` | number |  |
| `items[].createdAt` | string |  |
| `items[].discounts` | array |  |
| `items[].discountTotal` | number |  |
| `items[].id` | number |  |
| `items[].initialPrice` | number |  |
| `items[].markingObjects` | array |  |
| `items[].offer.displayName` | string |  |
| `items[].offer.id` | number |  |
| `items[].offer.name` | string |  |
| `items[].offer.quantity` | number |  |
| `items[].offer.unit.code` | string |  |
| `items[].offer.unit.name` | string |  |
| `items[].offer.unit.sym` | string |  |
| `items[].offer.xmlId` | string |  |
| `items[].ordering` | number |  |
| `items[].prices[].price` | number |  |
| `items[].prices[].quantity` | number |  |
| `items[].properties` | array |  |
| `items[].purchasePrice` | number |  |
| `items[].quantity` | number |  |
| `items[].status` | string |  |
| `lastName` | string |  |
| `managerComment` | string |  |
| `managerId` | number |  |
| `markDatetime` | string |  |
| `number` | string |  |
| `orderMethod` | string |  |
| `orderType` | string |  |
| `payments` | object |  |
| `phone` | string |  |
| `prepaySum` | number |  |
| `privilegeType` | string |  |
| `purchaseSumm` | number |  |
| `shipped` | boolean |  |
| `site` | string |  |
| `slug` | number |  |
| `status` | string |  |
| `statusUpdatedAt` | string |  |
| `summ` | number |  |
| `totalSumm` | number |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /orders/:externalId` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

