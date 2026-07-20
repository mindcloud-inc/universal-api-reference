# Apollo: Bulk Organization Enrichment

Retrieves enriched data for up to 10 organizations from Apollo.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-organization-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-organization-enrichment?connectionId=$CONNECTION_ID&domains%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domains[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-organization-enrichment?${params}`, {
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
| `domains[]` | array<string> | yes | Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": {},
      "errorMessage": {},
      "missingRecords": 1,
      "organizations": [
        {
          "alexaRanking": {},
          "angellistUrl": {},
          "blogUrl": {},
          "city": "string",
          "country": "string",
          "crunchbaseUrl": {},
          "departmentalHeadCount": {
            "accounting": 1,
            "administrative": 1,
            "artsAndDesign": 1,
            "businessDevelopment": 1,
            "consulting": 1,
            "dataScience": 1,
            "education": 1,
            "engineering": 1,
            "entrepreneurship": 1,
            "finance": 1,
            "humanResources": 1,
            "informationTechnology": 1,
            "legal": 1,
            "marketing": 1,
            "mediaAndCommmunication": 1,
            "operations": 1,
            "productManagement": 1,
            "sales": 1,
            "support": 1
          },
          "estimatedNumEmployees": 1,
          "facebookUrl": "https://example.com",
          "foundedYear": {},
          "hasIntentSignalAccount": true,
          "id": "string",
          "industries": [
            "string"
          ],
          "industry": "string",
          "industryTagId": "string",
          "intentSignalAccount": {},
          "intentStrength": {},
          "keywords": [
            "string"
          ],
          "languages": [
            "string"
          ],
          "linkedinUid": "https://example.com",
          "linkedinUrl": "https://example.com",
          "logoUrl": "https://example.com",
          "name": "Ava Chen",
          "organizationHeadcountSixMonthGrowth": {},
          "organizationHeadcountTwelveMonthGrowth": {},
          "organizationHeadcountTwentyFourMonthGrowth": {},
          "organizationRevenue": 1,
          "organizationRevenuePrinted": "string",
          "ownedByOrganizationId": {},
          "phone": "string",
          "postalCode": "string",
          "primaryDomain": "string",
          "primaryPhone": {
            "number": "string",
            "sanitizedNumber": "string",
            "source": "string"
          },
          "publiclyTradedExchange": {},
          "publiclyTradedSymbol": {},
          "rawAddress": "string",
          "retailLocationCount": 1,
          "sanitizedPhone": "string",
          "shortDescription": "string",
          "showIntent": true,
          "snippetsLoaded": true,
          "state": "string",
          "streetAddress": "string",
          "twitterUrl": "https://example.com",
          "websiteUrl": "https://example.com"
        }
      ],
      "status": "string",
      "totalRequestedDomains": 1,
      "uniqueDomains": 1,
      "uniqueEnrichedRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | object |  |
| `errorMessage` | object |  |
| `missingRecords` | number |  |
| `organizations[].alexaRanking` | object |  |
| `organizations[].angellistUrl` | object |  |
| `organizations[].blogUrl` | object |  |
| `organizations[].city` | string |  |
| `organizations[].country` | string |  |
| `organizations[].crunchbaseUrl` | object |  |
| `organizations[].departmentalHeadCount.accounting` | number |  |
| `organizations[].departmentalHeadCount.administrative` | number |  |
| `organizations[].departmentalHeadCount.artsAndDesign` | number |  |
| `organizations[].departmentalHeadCount.businessDevelopment` | number |  |
| `organizations[].departmentalHeadCount.consulting` | number |  |
| `organizations[].departmentalHeadCount.dataScience` | number |  |
| `organizations[].departmentalHeadCount.education` | number |  |
| `organizations[].departmentalHeadCount.engineering` | number |  |
| `organizations[].departmentalHeadCount.entrepreneurship` | number |  |
| `organizations[].departmentalHeadCount.finance` | number |  |
| `organizations[].departmentalHeadCount.humanResources` | number |  |
| `organizations[].departmentalHeadCount.informationTechnology` | number |  |
| `organizations[].departmentalHeadCount.legal` | number |  |
| `organizations[].departmentalHeadCount.marketing` | number |  |
| `organizations[].departmentalHeadCount.mediaAndCommmunication` | number |  |
| `organizations[].departmentalHeadCount.operations` | number |  |
| `organizations[].departmentalHeadCount.productManagement` | number |  |
| `organizations[].departmentalHeadCount.sales` | number |  |
| `organizations[].departmentalHeadCount.support` | number |  |
| `organizations[].estimatedNumEmployees` | number |  |
| `organizations[].facebookUrl` | string |  |
| `organizations[].foundedYear` | object |  |
| `organizations[].hasIntentSignalAccount` | boolean |  |
| `organizations[].id` | string |  |
| `organizations[].industries[]` | string |  |
| `organizations[].industry` | string |  |
| `organizations[].industryTagId` | string |  |
| `organizations[].intentSignalAccount` | object |  |
| `organizations[].intentStrength` | object |  |
| `organizations[].keywords[]` | string |  |
| `organizations[].languages[]` | string |  |
| `organizations[].linkedinUid` | string |  |
| `organizations[].linkedinUrl` | string |  |
| `organizations[].logoUrl` | string |  |
| `organizations[].name` | string |  |
| `organizations[].organizationHeadcountSixMonthGrowth` | object |  |
| `organizations[].organizationHeadcountTwelveMonthGrowth` | object |  |
| `organizations[].organizationHeadcountTwentyFourMonthGrowth` | object |  |
| `organizations[].organizationRevenue` | number |  |
| `organizations[].organizationRevenuePrinted` | string |  |
| `organizations[].ownedByOrganizationId` | object |  |
| `organizations[].phone` | string |  |
| `organizations[].postalCode` | string |  |
| `organizations[].primaryDomain` | string |  |
| `organizations[].primaryPhone.number` | string |  |
| `organizations[].primaryPhone.sanitizedNumber` | string |  |
| `organizations[].primaryPhone.source` | string |  |
| `organizations[].publiclyTradedExchange` | object |  |
| `organizations[].publiclyTradedSymbol` | object |  |
| `organizations[].rawAddress` | string |  |
| `organizations[].retailLocationCount` | number |  |
| `organizations[].sanitizedPhone` | string |  |
| `organizations[].shortDescription` | string |  |
| `organizations[].showIntent` | boolean |  |
| `organizations[].snippetsLoaded` | boolean |  |
| `organizations[].state` | string |  |
| `organizations[].streetAddress` | string |  |
| `organizations[].twitterUrl` | string |  |
| `organizations[].websiteUrl` | string |  |
| `status` | string |  |
| `totalRequestedDomains` | number |  |
| `uniqueDomains` | number |  |
| `uniqueEnrichedRecords` | number |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/organizations/bulk_enrich` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-organization-enrichment.md) for the provider-specific parameters and requirements.

