# Apollo: People API Search



```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/people-api-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/people-api-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/people-api-search?${params}`, {
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
| `personTitles[]` | array<string> | no |  |
| `includeSimilarTitles` | boolean | no |  |
| `organizationIds[]` | array<string> | no |  |
| `qOrganizationDomainsList[]` | array<string> | no |  |
| `personSeniorities` | list<string> | no | One of: `c_suite`, `director`, `entry`, `founder`, `head`, `intern`, `manager`, `owner`, `partner`, `senior`, `vp`. Accepts multiple values as an array. |
| `personLocations[]` | array<string> | no |  |
| `organizationLocations[]` | array<string> | no |  |
| `organizationNumEmployeesRanges[]` | array<string> | no |  |
| `contactEmailStatus` | list<string> | no | One of: `likely to engage`, `unavailable`, `unverified`, `verified`. Accepts multiple values as an array. |
| `qPersonName` | string | no |  |
| `currentlyUsingAnyOfTechnologyUids[]` | array<string> | no |  |
| `notOrganizationWebsitesList[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "hasCity": true,
      "hasCountry": true,
      "hasDirectPhone": "string",
      "hasEmail": true,
      "hasState": true,
      "id": "string",
      "lastNameObfuscated": "Chen",
      "lastRefreshedAt": "string",
      "organization": {
        "hasCity": true,
        "hasCountry": true,
        "hasEmployeeCount": true,
        "hasIndustry": true,
        "hasPhone": true,
        "hasRevenue": true,
        "hasState": true,
        "hasZipCode": true,
        "name": "Ava Chen"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string |  |
| `hasCity` | boolean |  |
| `hasCountry` | boolean |  |
| `hasDirectPhone` | string |  |
| `hasEmail` | boolean |  |
| `hasState` | boolean |  |
| `id` | string |  |
| `lastNameObfuscated` | string |  |
| `lastRefreshedAt` | string |  |
| `organization` | object |  |
| `organization.hasCity` | boolean |  |
| `organization.hasCountry` | boolean |  |
| `organization.hasEmployeeCount` | boolean |  |
| `organization.hasIndustry` | boolean |  |
| `organization.hasPhone` | boolean |  |
| `organization.hasRevenue` | boolean |  |
| `organization.hasState` | boolean |  |
| `organization.hasZipCode` | boolean |  |
| `organization.name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/mixed_people/api_search` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/people-api-search.md) for the provider-specific parameters and requirements.

