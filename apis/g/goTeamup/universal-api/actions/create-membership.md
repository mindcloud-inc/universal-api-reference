# GoTeamup: Create Membership

Creates a new membership in GoTeamup.

```
POST https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-membership" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string",
  "category": 1,
  "allowRepeatPurchases": true,
  "visibleToCustomers": true,
  "purchasableOnlyByProvider": true,
  "newCustomersOnly": true,
  "oneTimeFee": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-membership', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string",
    "category": 1,
    "allowRepeatPurchases": true,
    "visibleToCustomers": true,
    "purchasableOnlyByProvider": true,
    "newCustomersOnly": true,
    "oneTimeFee": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Membership name |
| `type` | string | yes | Membership type |
| `category` | number | yes | Membership category |
| `allowRepeatPurchases` | boolean | yes | Whether repeat purchases are allowed |
| `visibleToCustomers` | boolean | yes | Whether customers can see the membership |
| `purchasableOnlyByProvider` | boolean | yes | Whether only providers can purchase the membership |
| `newCustomersOnly` | boolean | yes | Whether only new customers can purchase the membership |
| `oneTimeFee` | number | yes | One-time fee amount |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeMemberCount": 1,
      "allotment": "string",
      "allowRepeatPurchases": true,
      "beginOnFirstRegistration": true,
      "category": 1,
      "description": "string",
      "displayPrice": {
        "currencySymbol": "string",
        "currencySymbolPosition": "string",
        "decimal": 1,
        "isoCurrencyCode": "string",
        "string": "string"
      },
      "duration": {},
      "durationUnit": {},
      "expirationDate": {},
      "forSale": true,
      "hasActiveMembers": true,
      "id": 1,
      "incompleteReasons": [
        "string"
      ],
      "isDraft": true,
      "isDropin": true,
      "name": "Ava Chen",
      "newCustomersOnly": true,
      "object": "string",
      "oneTimeFee": {
        "currencySymbol": "string",
        "currencySymbolPosition": "string",
        "decimal": 1,
        "isoCurrencyCode": "string",
        "string": "string"
      },
      "penaltySystem": {},
      "plans": "string",
      "price": {
        "currencySymbol": "string",
        "currencySymbolPosition": "string",
        "decimal": 1,
        "isoCurrencyCode": "string",
        "string": "string"
      },
      "purchasableOnlyByProvider": true,
      "shareable": true,
      "startDate": {},
      "terms": "string",
      "type": "string",
      "useProrate": true,
      "visibleToCustomers": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeMemberCount` | number |  |
| `allotment` | string |  |
| `allowRepeatPurchases` | boolean |  |
| `beginOnFirstRegistration` | boolean |  |
| `category` | number |  |
| `description` | string |  |
| `displayPrice.currencySymbol` | string |  |
| `displayPrice.currencySymbolPosition` | string |  |
| `displayPrice.decimal` | number |  |
| `displayPrice.isoCurrencyCode` | string |  |
| `displayPrice.string` | string |  |
| `duration` | object |  |
| `durationUnit` | object |  |
| `expirationDate` | object |  |
| `forSale` | boolean |  |
| `hasActiveMembers` | boolean |  |
| `id` | number |  |
| `incompleteReasons[]` | string |  |
| `isDraft` | boolean |  |
| `isDropin` | boolean |  |
| `name` | string |  |
| `newCustomersOnly` | boolean |  |
| `object` | string |  |
| `oneTimeFee.currencySymbol` | string |  |
| `oneTimeFee.currencySymbolPosition` | string |  |
| `oneTimeFee.decimal` | number |  |
| `oneTimeFee.isoCurrencyCode` | string |  |
| `oneTimeFee.string` | string |  |
| `penaltySystem` | object |  |
| `plans` | string |  |
| `price.currencySymbol` | string |  |
| `price.currencySymbolPosition` | string |  |
| `price.decimal` | number |  |
| `price.isoCurrencyCode` | string |  |
| `price.string` | string |  |
| `purchasableOnlyByProvider` | boolean |  |
| `shareable` | boolean |  |
| `startDate` | object |  |
| `terms` | string |  |
| `type` | string |  |
| `useProrate` | boolean |  |
| `visibleToCustomers` | boolean |  |

## Native endpoint

Through the native GoTeamup API, this operation is `POST /memberships` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-membership.md) for the provider-specific parameters and requirements.

