# GoTeamup: Retrieve Membership

Retrieves a membership from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-membership?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-membership?${params}`, {
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
| `id` | number | yes | The TeamUp membership ID |

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

Through the native GoTeamup API, this operation is `GET /memberships/:id` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-membership.md) for the provider-specific parameters and requirements.

