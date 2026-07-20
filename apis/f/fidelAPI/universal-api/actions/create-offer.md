# Fidel API: Create Offer

Creates a new offer in Fidel API.

```
POST https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "brandId": "string",
  "countryCode": "string",
  "name": "Ava Chen",
  "startDate": "string",
  "type.name": "Ava Chen",
  "type.value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-offer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "brandId": "string",
    "countryCode": "string",
    "name": "Ava Chen",
    "startDate": "string",
    "type.name": "Ava Chen",
    "type.value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `brandId` | string | yes |  |
| `countryCode` | string | yes | ISO 3166-1 alpha-3 country code where the offer is active. |
| `name` | string | yes | Name of the offer. |
| `startDate` | string | yes | Offer start date in YYYY-MM-DDThh:mm:ss format. |
| `type.name` | string | yes | Offer type name. |
| `type.value` | number | yes | Offer type value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accepted": true,
      "activation": {},
      "additionalTerms": "string",
      "brandId": "string",
      "brandLogoURL": "https://example.com",
      "brandName": "Ava Chen",
      "countryCode": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "daysOfWeek": [
        1
      ],
      "endDate": "2026-05-07T12:00:00.000Z",
      "feeSplit": 1,
      "funded": {},
      "id": "string",
      "live": true,
      "locationsTotal": 1,
      "maxTransactionAmount": 1,
      "minTransactionAmount": 1,
      "name": "Ava Chen",
      "origin": {},
      "priority": 1,
      "publisherId": "string",
      "returnPeriod": 1,
      "schemes": [
        "string"
      ],
      "startDate": "string",
      "supplier": "string",
      "transactionSource": "string",
      "type": {},
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted` | boolean |  |
| `activation` | object |  |
| `additionalTerms` | string |  |
| `brandId` | string |  |
| `brandLogoURL` | string |  |
| `brandName` | string |  |
| `countryCode` | string |  |
| `created` | date |  |
| `currency` | string |  |
| `daysOfWeek` | array<number> |  |
| `endDate` | date |  |
| `feeSplit` | number |  |
| `funded` | object |  |
| `id` | string |  |
| `live` | boolean |  |
| `locationsTotal` | number |  |
| `maxTransactionAmount` | number |  |
| `minTransactionAmount` | number |  |
| `name` | string |  |
| `origin` | object |  |
| `priority` | number |  |
| `publisherId` | string |  |
| `returnPeriod` | number |  |
| `schemes` | array<string> |  |
| `startDate` | string |  |
| `supplier` | string |  |
| `transactionSource` | string |  |
| `type` | object |  |
| `updated` | date |  |

## Native endpoint

Through the native Fidel API API, this operation is `POST /offers` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-offer.md) for the provider-specific parameters and requirements.

