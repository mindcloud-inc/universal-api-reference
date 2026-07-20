# Fidel API: List Offers

Retrieves offers from Fidel API.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-offers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-offers?${params}`, {
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
      "shortDescription": "string",
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
| `maxTransactionAmount` | number |  |
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
| `shortDescription` | string |  |
| `startDate` | string |  |
| `status` | string |  |
| `supplier` | string |  |
| `transactionSource` | string |  |
| `type` | object |  |
| `updated` | date |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /offers` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-offers.md) for the provider-specific parameters and requirements.

