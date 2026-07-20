# Apollo: Get Complete Organization Info

Retrieves complete organization information from Apollo.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-complete-organization-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-complete-organization-info?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-complete-organization-info?${params}`, {
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
| `id` | string | yes | The Apollo ID for the organization that you want to research. To find organization IDs, call the Organization Search endpoint and identify the `organizaton_id` value for the organization. Example: `5e66b6381e05b4008c8331b8` |

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
      "detailViewLoaded": true,
      "employeeMetrics": [
        {
          "departments": [
            {
              "churned": 1,
              "functions": {},
              "new": 1,
              "retained": 1
            }
          ],
          "startDate": {}
        }
      ],
      "estimatedNumEmployees": 1,
      "facebookUrl": {},
      "foundedYear": 1,
      "hasIntentSignalAccount": true,
      "id": "string",
      "industries": [
        "string"
      ],
      "industry": "string",
      "industryTagId": "string",
      "intentSignalAccount": {},
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
      "showIntent": true,
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
| `detailViewLoaded` | boolean |  |
| `employeeMetrics[].departments[].churned` | number |  |
| `employeeMetrics[].departments[].functions` | object |  |
| `employeeMetrics[].departments[].new` | number |  |
| `employeeMetrics[].departments[].retained` | number |  |
| `employeeMetrics[].startDate` | object |  |
| `estimatedNumEmployees` | number |  |
| `facebookUrl` | object |  |
| `foundedYear` | number |  |
| `hasIntentSignalAccount` | boolean |  |
| `id` | string |  |
| `industries[]` | string |  |
| `industry` | string |  |
| `industryTagId` | string |  |
| `intentSignalAccount` | object |  |
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
| `showIntent` | boolean |  |
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

Through the native Apollo API, this operation is `GET v1/organizations/:id` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-complete-organization-info.md) for the provider-specific parameters and requirements.

