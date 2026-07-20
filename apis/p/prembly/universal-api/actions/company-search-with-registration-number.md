# Prembly: Company Search With Registration Number

Creates a company search by registration number in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/company-search-with-registration-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/company-search-with-registration-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/company-search-with-registration-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountingAuthorityId": "string",
      "activityDescription": "string",
      "address": "string",
      "alternateNames": [
        "Ava Chen"
      ],
      "annualAssembly": "string",
      "authorizedCapital": "string",
      "brandName": "Ava Chen",
      "canSellShares": "string",
      "countryId": "string",
      "countyId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentEmployeesNumber": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateDisolved": "2026-05-07T12:00:00.000Z",
      "dateStatusChange": "2026-05-07T12:00:00.000Z",
      "endDateFinancialYear": "2026-05-07T12:00:00.000Z",
      "europeanNumber": "string",
      "exciseCancelDate": "2026-05-07T12:00:00.000Z",
      "exciseDate": "2026-05-07T12:00:00.000Z",
      "exciseNumber": "string",
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "financialYear": "2026-05-07T12:00:00.000Z",
      "hasPublicDebt": "string",
      "hideAddress": "string",
      "hideCompany": "string",
      "id": "string",
      "internationalNumber": "string",
      "localNumber": "string",
      "mailingAddress": "string",
      "name": "Ava Chen",
      "noindex": "string",
      "notes": "string",
      "oldInternationalNumber": "string",
      "paidShareCapital": 1,
      "paysExcise": "string",
      "paysVat": "string",
      "placeOfFormation": "string",
      "postalCode": 1,
      "profitRank": "string",
      "providerId": 1,
      "publicDebtAmount": 1,
      "registryUpdateDate": "2026-05-07T12:00:00.000Z",
      "sharesClass": "string",
      "sharesIssued": "string",
      "sharesNotes": "string",
      "sharesValue": "string",
      "shortName": "Ava Chen",
      "statusText": "string",
      "subscribedShareCapital": 1,
      "terms": "string",
      "turnoverRank": "string",
      "turnoverRankLastYear": "string",
      "typeId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedAtSitemap": "2026-05-07T12:00:00.000Z",
      "vatCancelDate": "2026-05-07T12:00:00.000Z",
      "vatDate": "2026-05-07T12:00:00.000Z",
      "vatNumber": "string",
      "vatRemovalBasis": "string",
      "vatRestorationBasis": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingAuthorityId` | string |  |
| `activityDescription` | string |  |
| `address` | string |  |
| `alternateNames[]` | string |  |
| `annualAssembly` | string |  |
| `authorizedCapital` | string |  |
| `brandName` | string |  |
| `canSellShares` | string |  |
| `countryId` | string |  |
| `countyId` | number |  |
| `createdAt` | date |  |
| `currentEmployeesNumber` | string |  |
| `dateCreated` | date |  |
| `dateDisolved` | date |  |
| `dateStatusChange` | date |  |
| `endDateFinancialYear` | date |  |
| `europeanNumber` | string |  |
| `exciseCancelDate` | date |  |
| `exciseDate` | date |  |
| `exciseNumber` | string |  |
| `expirationDate` | date |  |
| `financialYear` | date |  |
| `hasPublicDebt` | string |  |
| `hideAddress` | string |  |
| `hideCompany` | string |  |
| `id` | string |  |
| `internationalNumber` | string |  |
| `localNumber` | string |  |
| `mailingAddress` | string |  |
| `name` | string |  |
| `noindex` | string |  |
| `notes` | string |  |
| `oldInternationalNumber` | string |  |
| `paidShareCapital` | number |  |
| `paysExcise` | string |  |
| `paysVat` | string |  |
| `placeOfFormation` | string |  |
| `postalCode` | number |  |
| `profitRank` | string |  |
| `providerId` | number |  |
| `publicDebtAmount` | number |  |
| `registryUpdateDate` | date |  |
| `sharesClass` | string |  |
| `sharesIssued` | string |  |
| `sharesNotes` | string |  |
| `sharesValue` | string |  |
| `shortName` | string |  |
| `statusText` | string |  |
| `subscribedShareCapital` | number |  |
| `terms` | string |  |
| `turnoverRank` | string |  |
| `turnoverRankLastYear` | string |  |
| `typeId` | number |  |
| `updatedAt` | date |  |
| `updatedAtSitemap` | date |  |
| `vatCancelDate` | date |  |
| `vatDate` | date |  |
| `vatNumber` | string |  |
| `vatRemovalBasis` | string |  |
| `vatRestorationBasis` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /verification/global/company` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/company-search-with-registration-number.md) for the provider-specific parameters and requirements.

