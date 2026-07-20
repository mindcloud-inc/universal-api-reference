# Fidel API: Get Offer

Retrieves an offer from Fidel API.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-offer?connectionId=$CONNECTION_ID&offerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "offerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-offer?${params}`, {
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
| `offerId` | string | yes |  |

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
      "metadata": {},
      "minTransactionAmount": 1,
      "name": "Ava Chen",
      "origin": {},
      "priority": 1,
      "programId": "string",
      "programName": "Ava Chen",
      "publisherId": "string",
      "returnPeriod": 1,
      "schemes": [
        "string"
      ],
      "startDate": "string",
      "status": "string",
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
| `metadata` | object |  |
| `minTransactionAmount` | number |  |
| `name` | string |  |
| `origin` | object |  |
| `priority` | number |  |
| `programId` | string |  |
| `programName` | string |  |
| `publisherId` | string |  |
| `returnPeriod` | number |  |
| `schemes` | array<string> |  |
| `startDate` | string |  |
| `status` | string |  |
| `supplier` | string |  |
| `transactionSource` | string |  |
| `type` | object |  |
| `updated` | date |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /offers/:offerId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-offer.md) for the provider-specific parameters and requirements.

