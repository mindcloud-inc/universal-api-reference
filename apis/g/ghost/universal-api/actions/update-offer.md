# Ghost: Update Offer

Updates an existing offer in Ghost.

```
PUT https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/update-offer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `offers[0].name` | string | no |  |
| `offers[0].code` | string | no |  |
| `offers[0].displayTitle` | string | no |  |
| `offers[0].displayDescription` | string | no |  |

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
        "id": "string",
        "name": "Ava Chen"
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
| `tier.name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `PUT /offers/:id/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-offer.md) for the provider-specific parameters and requirements.

