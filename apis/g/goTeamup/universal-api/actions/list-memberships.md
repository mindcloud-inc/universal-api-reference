# GoTeamup: List Memberships

Finds memberships in GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-memberships?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-memberships?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": {},
      "previous": {},
      "results": [
        {
          "activeMemberCount": {},
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `next` | object |  |
| `previous` | object |  |
| `results[].activeMemberCount` | object |  |
| `results[].allotment` | string |  |
| `results[].allowRepeatPurchases` | boolean |  |
| `results[].beginOnFirstRegistration` | boolean |  |
| `results[].category` | number |  |
| `results[].description` | string |  |
| `results[].displayPrice.currencySymbol` | string |  |
| `results[].displayPrice.currencySymbolPosition` | string |  |
| `results[].displayPrice.decimal` | number |  |
| `results[].displayPrice.isoCurrencyCode` | string |  |
| `results[].displayPrice.string` | string |  |
| `results[].duration` | object |  |
| `results[].durationUnit` | object |  |
| `results[].expirationDate` | object |  |
| `results[].forSale` | boolean |  |
| `results[].hasActiveMembers` | boolean |  |
| `results[].id` | number |  |
| `results[].incompleteReasons[]` | string |  |
| `results[].isDraft` | boolean |  |
| `results[].isDropin` | boolean |  |
| `results[].name` | string |  |
| `results[].newCustomersOnly` | boolean |  |
| `results[].object` | string |  |
| `results[].oneTimeFee.currencySymbol` | string |  |
| `results[].oneTimeFee.currencySymbolPosition` | string |  |
| `results[].oneTimeFee.decimal` | number |  |
| `results[].oneTimeFee.isoCurrencyCode` | string |  |
| `results[].oneTimeFee.string` | string |  |
| `results[].penaltySystem` | object |  |
| `results[].plans` | string |  |
| `results[].price.currencySymbol` | string |  |
| `results[].price.currencySymbolPosition` | string |  |
| `results[].price.decimal` | number |  |
| `results[].price.isoCurrencyCode` | string |  |
| `results[].price.string` | string |  |
| `results[].purchasableOnlyByProvider` | boolean |  |
| `results[].shareable` | boolean |  |
| `results[].startDate` | object |  |
| `results[].terms` | string |  |
| `results[].type` | string |  |
| `results[].useProrate` | boolean |  |
| `results[].visibleToCustomers` | boolean |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /memberships` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-memberships.md) for the provider-specific parameters and requirements.

