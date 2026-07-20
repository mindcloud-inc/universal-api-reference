# Apollo: View an Account

Retrieves an account record from Apollo.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/view-an-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/view-an-account?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/view-an-account?${params}`, {
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
| `id` | string | yes | The Apollo ID for the account that you want to retrieve. To find account IDs, call the Search for Accounts endpoint and identify the `id` value for the account. Example: `6518c6184f20350001a0b9c0` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "accountStageId": "string",
        "alexaRanking": 1,
        "angellistUrl": {},
        "blogUrl": {},
        "city": "string",
        "country": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "creatorId": "string",
        "crmOwnerId": {},
        "crmRecordUrl": {},
        "crunchbaseUrl": {},
        "currentTechnologies": [
          {
            "category": "string",
            "name": "Ava Chen",
            "uid": "string"
          }
        ],
        "disableFlag": true,
        "domain": "string",
        "engagementGraph": {},
        "estimatedNumEmployees": 1,
        "existenceLevel": "string",
        "facebookUrl": {},
        "foundedYear": {},
        "hubspotId": {},
        "id": "string",
        "industries": [
          "string"
        ],
        "industry": "string",
        "industryTagId": "string",
        "intentStrength": {},
        "languages": [
          "string"
        ],
        "latestFundingRoundDate": {},
        "latestFundingStage": {},
        "linkedinUid": "https://example.com",
        "linkedinUrl": "https://example.com",
        "logoUrl": "https://example.com",
        "modality": "string",
        "name": "Ava Chen",
        "numContacts": 1,
        "numSuborganizations": 1,
        "organizationCity": "string",
        "organizationCountry": "string",
        "organizationHeadcountSixMonthGrowth": {},
        "organizationHeadcountTwelveMonthGrowth": {},
        "organizationHeadcountTwentyFourMonthGrowth": {},
        "organizationId": "string",
        "organizationPostalCode": "string",
        "organizationRawAddress": "string",
        "organizationRevenue": 1,
        "organizationRevenuePrinted": {},
        "organizationState": "string",
        "organizationStreetAddress": "string",
        "orgChartRemoved": true,
        "orgChartRootPeopleIds": [
          "string"
        ],
        "orgChartSector": "string",
        "orgChartShowDepartmentFilter": true,
        "originalSource": "string",
        "ownedByOrganizationId": {},
        "ownerId": "string",
        "parentAccountId": {},
        "phone": {},
        "phoneStatus": "string",
        "postalCode": "string",
        "primaryDomain": "string",
        "publiclyTradedExchange": {},
        "publiclyTradedSymbol": {},
        "rawAddress": "string",
        "retailLocationCount": 1,
        "salesforceId": {},
        "shortDescription": "string",
        "showIntent": true,
        "snippetsLoaded": true,
        "source": "string",
        "sourceDisplayName": "Ava Chen",
        "state": "string",
        "streetAddress": "string",
        "suggestedFromRuleEngineConfigId": {},
        "suggestLocationEnrichment": true,
        "teamId": "string",
        "technologyNames": [
          "Ava Chen"
        ],
        "totalFunding": {},
        "totalFundingPrinted": {},
        "twitterUrl": {},
        "websiteUrl": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.accountStageId` | string |  |
| `account.alexaRanking` | number |  |
| `account.angellistUrl` | object |  |
| `account.blogUrl` | object |  |
| `account.city` | string |  |
| `account.country` | string |  |
| `account.createdAt` | date |  |
| `account.creatorId` | string |  |
| `account.crmOwnerId` | object |  |
| `account.crmRecordUrl` | object |  |
| `account.crunchbaseUrl` | object |  |
| `account.currentTechnologies[].category` | string |  |
| `account.currentTechnologies[].name` | string |  |
| `account.currentTechnologies[].uid` | string |  |
| `account.disableFlag` | boolean |  |
| `account.domain` | string |  |
| `account.engagementGraph` | object |  |
| `account.estimatedNumEmployees` | number |  |
| `account.existenceLevel` | string |  |
| `account.facebookUrl` | object |  |
| `account.foundedYear` | object |  |
| `account.hubspotId` | object |  |
| `account.id` | string |  |
| `account.industries[]` | string |  |
| `account.industry` | string |  |
| `account.industryTagId` | string |  |
| `account.intentStrength` | object |  |
| `account.languages[]` | string |  |
| `account.latestFundingRoundDate` | object |  |
| `account.latestFundingStage` | object |  |
| `account.linkedinUid` | string |  |
| `account.linkedinUrl` | string |  |
| `account.logoUrl` | string |  |
| `account.modality` | string |  |
| `account.name` | string |  |
| `account.numContacts` | number |  |
| `account.numSuborganizations` | number |  |
| `account.organizationCity` | string |  |
| `account.organizationCountry` | string |  |
| `account.organizationHeadcountSixMonthGrowth` | object |  |
| `account.organizationHeadcountTwelveMonthGrowth` | object |  |
| `account.organizationHeadcountTwentyFourMonthGrowth` | object |  |
| `account.organizationId` | string |  |
| `account.organizationPostalCode` | string |  |
| `account.organizationRawAddress` | string |  |
| `account.organizationRevenue` | number |  |
| `account.organizationRevenuePrinted` | object |  |
| `account.organizationState` | string |  |
| `account.organizationStreetAddress` | string |  |
| `account.orgChartRemoved` | boolean |  |
| `account.orgChartRootPeopleIds[]` | string |  |
| `account.orgChartSector` | string |  |
| `account.orgChartShowDepartmentFilter` | boolean |  |
| `account.originalSource` | string |  |
| `account.ownedByOrganizationId` | object |  |
| `account.ownerId` | string |  |
| `account.parentAccountId` | object |  |
| `account.phone` | object |  |
| `account.phoneStatus` | string |  |
| `account.postalCode` | string |  |
| `account.primaryDomain` | string |  |
| `account.publiclyTradedExchange` | object |  |
| `account.publiclyTradedSymbol` | object |  |
| `account.rawAddress` | string |  |
| `account.retailLocationCount` | number |  |
| `account.salesforceId` | object |  |
| `account.shortDescription` | string |  |
| `account.showIntent` | boolean |  |
| `account.snippetsLoaded` | boolean |  |
| `account.source` | string |  |
| `account.sourceDisplayName` | string |  |
| `account.state` | string |  |
| `account.streetAddress` | string |  |
| `account.suggestedFromRuleEngineConfigId` | object |  |
| `account.suggestLocationEnrichment` | boolean |  |
| `account.teamId` | string |  |
| `account.technologyNames[]` | string |  |
| `account.totalFunding` | object |  |
| `account.totalFundingPrinted` | object |  |
| `account.twitterUrl` | object |  |
| `account.websiteUrl` | string |  |

## Native endpoint

Through the native Apollo API, this operation is `GET v1/accounts/:id` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-an-account.md) for the provider-specific parameters and requirements.

