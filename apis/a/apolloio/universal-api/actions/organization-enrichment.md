# Apollo: Organization Enrichment

Retrieves enriched data for an organization from Apollo.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/organization-enrichment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/organization-enrichment?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/organization-enrichment?${params}`, {
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
| `domain` | string | yes | The domain of the company that you want to enrich. Do not include `www.`, the `@` symbol, or similar. Example: `apollo.io` or `microsoft.com` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alexaRanking": 1,
      "angellistUrl": {},
      "blogUrl": {},
      "city": "string",
      "country": "string",
      "crunchbaseUrl": {},
      "currentTechnologies": [
        {
          "category": "string",
          "name": "Ava Chen",
          "uid": "string"
        }
      ],
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
      "facebookUrl": {},
      "foundedYear": 1,
      "id": "string",
      "industries": [
        "string"
      ],
      "industry": "string",
      "industryTagId": "string",
      "keywords": [
        "string"
      ],
      "languages": [
        "string"
      ],
      "latestFundingRoundDate": {},
      "latestFundingStage": {},
      "linkedinUid": "https://example.com",
      "linkedinUrl": "https://example.com",
      "logoUrl": "https://example.com",
      "naicsCodes": [
        "string"
      ],
      "name": "Ava Chen",
      "numSuborganizations": 1,
      "organizationRevenue": 1,
      "organizationRevenuePrinted": {},
      "orgChartRemoved": {},
      "orgChartRootPeopleIds": [
        "string"
      ],
      "orgChartSector": {},
      "orgChartShowDepartmentFilter": {},
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
      "sicCodes": [
        "string"
      ],
      "snippetsLoaded": true,
      "state": "string",
      "streetAddress": "string",
      "technologyNames": [
        "Ava Chen"
      ],
      "totalFunding": {},
      "totalFundingPrinted": {},
      "twitterUrl": "https://example.com",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alexaRanking` | number |  |
| `angellistUrl` | object |  |
| `blogUrl` | object |  |
| `city` | string |  |
| `country` | string |  |
| `crunchbaseUrl` | object |  |
| `currentTechnologies[].category` | string |  |
| `currentTechnologies[].name` | string |  |
| `currentTechnologies[].uid` | string |  |
| `departmentalHeadCount.accounting` | number |  |
| `departmentalHeadCount.administrative` | number |  |
| `departmentalHeadCount.artsAndDesign` | number |  |
| `departmentalHeadCount.businessDevelopment` | number |  |
| `departmentalHeadCount.consulting` | number |  |
| `departmentalHeadCount.dataScience` | number |  |
| `departmentalHeadCount.education` | number |  |
| `departmentalHeadCount.engineering` | number |  |
| `departmentalHeadCount.entrepreneurship` | number |  |
| `departmentalHeadCount.finance` | number |  |
| `departmentalHeadCount.humanResources` | number |  |
| `departmentalHeadCount.informationTechnology` | number |  |
| `departmentalHeadCount.legal` | number |  |
| `departmentalHeadCount.marketing` | number |  |
| `departmentalHeadCount.mediaAndCommmunication` | number |  |
| `departmentalHeadCount.operations` | number |  |
| `departmentalHeadCount.productManagement` | number |  |
| `departmentalHeadCount.sales` | number |  |
| `departmentalHeadCount.support` | number |  |
| `estimatedNumEmployees` | number |  |
| `facebookUrl` | object |  |
| `foundedYear` | number |  |
| `id` | string |  |
| `industries[]` | string |  |
| `industry` | string |  |
| `industryTagId` | string |  |
| `keywords[]` | string |  |
| `languages[]` | string |  |
| `latestFundingRoundDate` | object |  |
| `latestFundingStage` | object |  |
| `linkedinUid` | string |  |
| `linkedinUrl` | string |  |
| `logoUrl` | string |  |
| `naicsCodes[]` | string |  |
| `name` | string |  |
| `numSuborganizations` | number |  |
| `organizationRevenue` | number |  |
| `organizationRevenuePrinted` | object |  |
| `orgChartRemoved` | object |  |
| `orgChartRootPeopleIds[]` | string |  |
| `orgChartSector` | object |  |
| `orgChartShowDepartmentFilter` | object |  |
| `ownedByOrganizationId` | object |  |
| `phone` | string |  |
| `postalCode` | string |  |
| `primaryDomain` | string |  |
| `primaryPhone.number` | string |  |
| `primaryPhone.sanitizedNumber` | string |  |
| `primaryPhone.source` | string |  |
| `publiclyTradedExchange` | object |  |
| `publiclyTradedSymbol` | object |  |
| `rawAddress` | string |  |
| `retailLocationCount` | number |  |
| `sanitizedPhone` | string |  |
| `shortDescription` | string |  |
| `sicCodes[]` | string |  |
| `snippetsLoaded` | boolean |  |
| `state` | string |  |
| `streetAddress` | string |  |
| `technologyNames[]` | string |  |
| `totalFunding` | object |  |
| `totalFundingPrinted` | object |  |
| `twitterUrl` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Apollo API, this operation is `GET v1/organizations/enrich` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/organization-enrichment.md) for the provider-specific parameters and requirements.

