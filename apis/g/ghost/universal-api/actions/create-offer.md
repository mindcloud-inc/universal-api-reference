# Ghost: Create Offer

Creates a new offer in Ghost.

```
POST https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "offers[0].name": "Ava Chen",
  "offers[0].code": "string",
  "offers[0].type": "string",
  "offers[0].cadence": "string",
  "offers[0].amount": 1,
  "offers[0].duration": "string",
  "offers[0].tier.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-offer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "offers[0].name": "Ava Chen",
    "offers[0].code": "string",
    "offers[0].type": "string",
    "offers[0].cadence": "string",
    "offers[0].amount": 1,
    "offers[0].duration": "string",
    "offers[0].tier.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offers[0].name` | string | yes |  |
| `offers[0].code` | string | yes |  |
| `offers[0].displayTitle` | string | no |  |
| `offers[0].displayDescription` | string | no |  |
| `offers[0].type` | string | yes |  |
| `offers[0].cadence` | string | yes |  |
| `offers[0].amount` | number | yes |  |
| `offers[0].duration` | string | yes |  |
| `offers[0].tier.id` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offers[0].durationInMonths` | number | no |  |
| `offers[0].currencyRestriction` | boolean | no |  |
| `offers[0].currency` | string | no |  |
| `offers[0].status` | string | no |  |
| `offers[0].redemptionCount` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cadence": "string",
      "code": "string",
      "createdAt": "string",
      "currency": {},
      "currencyRestriction": true,
      "displayDescription": "string",
      "displayTitle": "string",
      "duration": "string",
      "durationInMonths": {},
      "id": "string",
      "lastRedeemed": {},
      "name": "Ava Chen",
      "redemptionCount": 1,
      "redemptionType": "string",
      "status": "string",
      "tier": {
        "id": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `cadence` | string |  |
| `code` | string |  |
| `createdAt` | string |  |
| `currency` | object |  |
| `currencyRestriction` | boolean |  |
| `displayDescription` | string |  |
| `displayTitle` | string |  |
| `duration` | string |  |
| `durationInMonths` | object |  |
| `id` | string |  |
| `lastRedeemed` | object |  |
| `name` | string |  |
| `redemptionCount` | number |  |
| `redemptionType` | string |  |
| `status` | string |  |
| `tier.id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `POST /offers/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-offer.md) for the provider-specific parameters and requirements.

