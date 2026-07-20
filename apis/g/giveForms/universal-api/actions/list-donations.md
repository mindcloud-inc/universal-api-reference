# GiveForms: List Donations

Finds donations for your organization in GiveForms.

```
GET https://connect.mindcloud.co/v1/universal/giveForms/latest/actions/list-donations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GiveForms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giveForms/latest/actions/list-donations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giveForms/latest/actions/list-donations?${params}`, {
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
      "address": "string",
      "amount": "string",
      "anonymous": true,
      "appFee": 1,
      "city": "string",
      "convertedAmount": "string",
      "convertedCurrency": "string",
      "country": "string",
      "currency": "string",
      "donationDate": "2026-05-07T12:00:00.000Z",
      "donationHonor": {},
      "donationType": "string",
      "email": "ava@example.com",
      "expMonth": 1,
      "expYear": 1,
      "feeCovered": "string",
      "firstName": "Ava",
      "formattedAmount": "string",
      "formattedAppFee": "string",
      "formattedConvertedAmount": "string",
      "formattedProcessingFee": "string",
      "formName": "Ava Chen",
      "id": 1,
      "last4": "string",
      "lastName": "Chen",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "paymentChargeId": "string",
      "paymentType": "string",
      "postcode": "string",
      "processingFee": 1,
      "questions": [
        {}
      ],
      "recurring": true,
      "state": "string",
      "status": "string",
      "timezone": "string",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmSource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `amount` | string |  |
| `anonymous` | boolean |  |
| `appFee` | number |  |
| `city` | string |  |
| `convertedAmount` | string |  |
| `convertedCurrency` | string |  |
| `country` | string |  |
| `currency` | string |  |
| `donationDate` | date |  |
| `donationHonor` | object |  |
| `donationType` | string |  |
| `email` | string |  |
| `expMonth` | number |  |
| `expYear` | number |  |
| `feeCovered` | string |  |
| `firstName` | string |  |
| `formattedAmount` | string |  |
| `formattedAppFee` | string |  |
| `formattedConvertedAmount` | string |  |
| `formattedProcessingFee` | string |  |
| `formName` | string |  |
| `id` | number |  |
| `last4` | string |  |
| `lastName` | string |  |
| `lastUpdatedAt` | date |  |
| `paymentChargeId` | string |  |
| `paymentType` | string |  |
| `postcode` | string |  |
| `processingFee` | number |  |
| `questions` | array<object> |  |
| `recurring` | boolean |  |
| `state` | string |  |
| `status` | string |  |
| `timezone` | string |  |
| `utmCampaign` | string |  |
| `utmContent` | string |  |
| `utmMedium` | string |  |
| `utmSource` | string |  |

## Native endpoint

Through the native GiveForms API, this operation is `GET /donations` (base URL `https://app.giveforms.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-donations.md) for the provider-specific parameters and requirements.

