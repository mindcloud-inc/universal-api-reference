# BetterContact: Get Enrichment Results

Retrieves BetterContact enrichment results by request ID.

```
GET https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/get-enrichment-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BetterContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/get-enrichment-results?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterContact/latest/actions/get-enrichment-results?${params}`, {
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
| `requestId` | string | yes | The BetterContact enrichment request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsLeft": "string",
      "data": [
        {
          "companyAbout": {},
          "companyAddressCity": {},
          "companyAddressCountry": {},
          "companyAddressState": {},
          "companyAddressStreet": {},
          "companyAddressZipcode": {},
          "companyCountryCode": {},
          "companyCrunchbaseUrl": {},
          "companyDescription": {},
          "companyDirectionsUrl": {},
          "companyDomain": "string",
          "companyEmployees": {},
          "companyEmployeesInLinkedin": {},
          "companyEmployeesNumber": {},
          "companyFollowers": {},
          "companyFormattedLocations": {},
          "companyFounded": {},
          "companyFunding": {},
          "companyHeadquarters": {},
          "companyHeadquartersAddress": {},
          "companyHeadquartersCity": {},
          "companyHeadquartersCountry": {},
          "companyId": {},
          "companyImage": {},
          "companyIndustries": {},
          "companyIndustryCode": {},
          "companyInvestors": {},
          "companyLegalId": {},
          "companyLegalName": {},
          "companyLinkedinId": {},
          "companyLinkedinUrl": {},
          "companyLogo": {},
          "companyName": "Ava Chen",
          "companyOrganizationType": {},
          "companyPhoneNumber": {},
          "companySimilar": {},
          "companySize": {},
          "companySpecialities": {},
          "companyStockInfo": {},
          "companyWebsite": {},
          "contactActivity": {},
          "contactAdditionalPhoneNumber": {},
          "contactAvatar": {},
          "contactCity": {},
          "contactConnections": {},
          "contactCountry": {},
          "contactCountryCode": {},
          "contactCurrentCompany": {},
          "contactEmailAddress": "ava@example.com",
          "contactEmailAddressProvider": "ava@example.com",
          "contactEmailAddressStatus": "ava@example.com",
          "contactExperience": {},
          "contactFirstName": "Ava",
          "contactFollowers": {},
          "contactFullName": "Ava Chen",
          "contactGender": {},
          "contactId": 1,
          "contactJobTitle": {},
          "contactLastName": "Chen",
          "contactLinkedinId": {},
          "contactLinkedinProfileUrl": "https://example.com",
          "contactLocation": {},
          "contactPeopleAlsoViewed": {},
          "contactPhoneNumber": {},
          "contactPhoneNumberCc": {},
          "contactPhoneNumberProvider": {},
          "contactPostalCode": {},
          "contactPosts": {},
          "doNotContact": true,
          "emailProvider": "ava@example.com",
          "enriched": true,
          "lastPhoneVerificationDate": {}
        }
      ],
      "id": "string",
      "status": "string",
      "summary": {
        "catchAllNotSafe": 1,
        "catchAllSafe": 1,
        "emailEnrichment": {
          "enriched": 1,
          "notEnriched": 1
        },
        "notFound": 1,
        "total": 1,
        "undeliverable": 1,
        "valid": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number |  |
| `creditsLeft` | string |  |
| `data[].companyAbout` | object |  |
| `data[].companyAddressCity` | object |  |
| `data[].companyAddressCountry` | object |  |
| `data[].companyAddressState` | object |  |
| `data[].companyAddressStreet` | object |  |
| `data[].companyAddressZipcode` | object |  |
| `data[].companyCountryCode` | object |  |
| `data[].companyCrunchbaseUrl` | object |  |
| `data[].companyDescription` | object |  |
| `data[].companyDirectionsUrl` | object |  |
| `data[].companyDomain` | string |  |
| `data[].companyEmployees` | object |  |
| `data[].companyEmployeesInLinkedin` | object |  |
| `data[].companyEmployeesNumber` | object |  |
| `data[].companyFollowers` | object |  |
| `data[].companyFormattedLocations` | object |  |
| `data[].companyFounded` | object |  |
| `data[].companyFunding` | object |  |
| `data[].companyHeadquarters` | object |  |
| `data[].companyHeadquartersAddress` | object |  |
| `data[].companyHeadquartersCity` | object |  |
| `data[].companyHeadquartersCountry` | object |  |
| `data[].companyId` | object |  |
| `data[].companyImage` | object |  |
| `data[].companyIndustries` | object |  |
| `data[].companyIndustryCode` | object |  |
| `data[].companyInvestors` | object |  |
| `data[].companyLegalId` | object |  |
| `data[].companyLegalName` | object |  |
| `data[].companyLinkedinId` | object |  |
| `data[].companyLinkedinUrl` | object |  |
| `data[].companyLogo` | object |  |
| `data[].companyName` | string |  |
| `data[].companyOrganizationType` | object |  |
| `data[].companyPhoneNumber` | object |  |
| `data[].companySimilar` | object |  |
| `data[].companySize` | object |  |
| `data[].companySpecialities` | object |  |
| `data[].companyStockInfo` | object |  |
| `data[].companyWebsite` | object |  |
| `data[].contactActivity` | object |  |
| `data[].contactAdditionalPhoneNumber` | object |  |
| `data[].contactAvatar` | object |  |
| `data[].contactCity` | object |  |
| `data[].contactConnections` | object |  |
| `data[].contactCountry` | object |  |
| `data[].contactCountryCode` | object |  |
| `data[].contactCurrentCompany` | object |  |
| `data[].contactEmailAddress` | string |  |
| `data[].contactEmailAddressProvider` | string |  |
| `data[].contactEmailAddressStatus` | string |  |
| `data[].contactExperience` | object |  |
| `data[].contactFirstName` | string |  |
| `data[].contactFollowers` | object |  |
| `data[].contactFullName` | string |  |
| `data[].contactGender` | object |  |
| `data[].contactId` | number |  |
| `data[].contactJobTitle` | object |  |
| `data[].contactLastName` | string |  |
| `data[].contactLinkedinId` | object |  |
| `data[].contactLinkedinProfileUrl` | string |  |
| `data[].contactLocation` | object |  |
| `data[].contactPeopleAlsoViewed` | object |  |
| `data[].contactPhoneNumber` | object |  |
| `data[].contactPhoneNumberCc` | object |  |
| `data[].contactPhoneNumberProvider` | object |  |
| `data[].contactPostalCode` | object |  |
| `data[].contactPosts` | object |  |
| `data[].doNotContact` | boolean |  |
| `data[].emailProvider` | string |  |
| `data[].enriched` | boolean |  |
| `data[].lastPhoneVerificationDate` | object |  |
| `id` | string |  |
| `status` | string |  |
| `summary.catchAllNotSafe` | number |  |
| `summary.catchAllSafe` | number |  |
| `summary.emailEnrichment.enriched` | number |  |
| `summary.emailEnrichment.notEnriched` | number |  |
| `summary.notFound` | number |  |
| `summary.total` | number |  |
| `summary.undeliverable` | number |  |
| `summary.valid` | number |  |

## Native endpoint

Through the native BetterContact API, this operation is `GET /async/:request_id` (base URL `https://app.bettercontact.rocks/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enrichment-results.md) for the provider-specific parameters and requirements.

