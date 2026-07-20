# Fidel API: Update Offer

Updates an existing offer in Fidel API.

```
PUT https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "offerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-offer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "offerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offerId` | string | yes |  |
| `name` | string | no | The offer name. |
| `shortDescription` | string | no | A short description for the offer. |
| `activation.enabled` | boolean | no | Whether activation is enabled. |
| `activation.qualifiedTransactionsLimit` | number | no | The number of qualified transactions required before the offer is redeemed. |

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
      "feeSplit": {},
      "funded": {},
      "id": "string",
      "live": true,
      "locationsTotal": 1,
      "maxTransactionAmount": 1,
      "metadata": {},
      "minTransactionAmount": 1,
      "name": "Ava Chen",
      "origin": {},
      "priority": 1,
      "programId": "string",
      "programName": "Ava Chen",
      "publisherId": "string",
      "returnPeriod": {},
      "schemes": [
        "string"
      ],
      "shortDescription": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "supplier": {},
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
| `feeSplit` | object |  |
| `funded` | object |  |
| `id` | string |  |
| `live` | boolean |  |
| `locationsTotal` | number |  |
| `maxTransactionAmount` | number |  |
| `metadata` | object |  |
| `minTransactionAmount` | number |  |
| `name` | string |  |
| `origin` | object |  |
| `priority` | number |  |
| `programId` | string |  |
| `programName` | string |  |
| `publisherId` | string |  |
| `returnPeriod` | object |  |
| `schemes` | array<string> |  |
| `shortDescription` | string |  |
| `startDate` | date |  |
| `status` | string |  |
| `supplier` | object |  |
| `transactionSource` | string |  |
| `type` | object |  |
| `updated` | date |  |

## Native endpoint

Through the native Fidel API API, this operation is `PATCH /offers/:offerId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-offer.md) for the provider-specific parameters and requirements.

