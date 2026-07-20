# Apollo: Organization Search

Finds organizations in Apollo by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/organization-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/organization-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/organization-search?${params}`, {
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
| `qOrganizationDomainsList[]` | array<string> | no | The domain name for the person's employer. This can be the current employer or a previous employer. Do not include `www.`, the `@` symbol, or similar. This parameter accepts up to 1,000 domains in a single request. Examples: `apollo.io`; `microsoft.com` |
| `organizationNumEmployeesRanges[]` | array<string> | no | The number range of employees working for the company. This enables you to find companies based on headcount. You can add multiple ranges to expand your search results. Each range you add needs to be a string, with the upper and lower numbers of the range separated only by a comma. Examples: `1,10`; `250,500`; `10000,20000` |
| `organizationLocations[]` | array<string> | no | The location of the company headquarters. You can search across cities, US states, and countries. If a company has several office locations, results are still based on the headquarters location. For example, if you search `chicago` but a company's HQ location is in `boston`, any Boston-based companies will not appearch in your search results, even if they match other parameters.. To exclude companies based on location, use the `organization_not_locations` parameter. Examples: `texas`; `tokyo`; `spain` |
| `organizationNotLocations[]` | array<string> | no | Exclude companies from search results based on the location of the company headquarters. You can use cities, US states, and countries as locations to exclude. This parameter is useful for ensuring you do not prospect in an undesirable territory. For example, if you use `ireland` as a value, no Ireland-based companies will appear in your search results. Examples: `minnesota`; `ireland`; `seoul` |
| `revenueRange[min]` | number | no | Search for organizations based on their revenue. Use this parameter to set the lower range of organization revenue. Use the `revenue_range[max]` parameter to set the upper range of revenue. Do not enter currency symbols, commas, or decimal points in the figure. Example: `300000` |
| `revenueRange[max]` | number | no | Search for organizations based on their revenue. Use this parameter to set the upper range of organization revenue. Use the `revenue_range[min]` parameter to set the lower range of revenue. Do not enter currency symbols, commas, or decimal points in the figure. Example: `50000000` |
| `currentlyUsingAnyOfTechnologyUids[]` | array<string> | no | Find organizations based on the technologies they currently use. Apollo supports filtering by 1,500+ technologies. Apollo calculates technologies data from multiple sources. This data is updated regularly. Check out the full list of supported technologies by downloading this CSV file . Use underscores (`_`) to replace spaces and periods for the technologies listed in the CSV file. Examples: `salesforce`; `google_analytics`; `wordpress_org` |
| `qOrganizationKeywordTags[]` | array<string> | no | Filter search results based on keywords associated with companies. For example, you can enter `mining` as a value to return only companies that have an association with the mining industry. Examples: `mining`; `sales strategy`; `consulting` |
| `qOrganizationName` | string | no | Filter search results to include a specific company name. If the value you enter for this parameter does not match with a company's name, the company will not appear in search results, even if it matches other parameters. Partial matches are accepted. For example, if you filter by the value `marketing`, a company called `NY Marketing Unlimited` would still be eligible as a search result, but `NY Market Analysis` would not be eligible. Example: `apollo` or `mining` |
| `organizationIds[]` | array<string> | no | The Apollo IDs for the companies you want to include in your search results. Each company in the Apollo database is assigned a unique ID. To find IDs, identify the values for `organization_id` when you call this endpoint. Example: `5e66b6381e05b4008c8331b8` |
| `latestFundingAmountRange[min]` | number | no | The minimum amount the company received with its most recent funding round. Use this parameter in combination with `latest_funding_amount_range[max]` to set a monetary range for the company's most recent funding round. Do not enter currency symbols, commas, or decimal points in the figure. Examples: `5000000`; `15000000` |
| `latestFundingAmountRange[max]` | number | no | The maximium amount the company received with its most recent funding round. Use this parameter in combination with `latest_funding_amount_range[min]` to set a monetary range for the company's most recent funding round. Do not enter currency symbols, commas, or decimal points in the figure. Examples: `5000000`; `15000000` |
| `totalFundingRange[min]` | number | no | The minimum amount the company received during all of its funding rounds combined. Use this parameter in combination with `total_funding_range[max]` to set a monetary range for all of the company's funding rounds. Do not enter currency symbols, commas, or decimal points in the figure. Examples: `50000000`; `350000000` |
| `totalFundingRange[max]` | number | no | The maximum amount the company received during all of its funding rounds combined. Use this parameter in combination with `total_funding_range[min]` to set a monetary range for all of the company's funding rounds. Do not enter currency symbols, commas, or decimal points in the figure. Examples: `50000000`; `350000000` |
| `latestFundingDateRange[min]` | date | no | The earliest date when the company received its most recent funding round. Use this parameter in combination with `latest_funding_date_range[max]` to set a date range for when the company received its most recent funding round. Example: `2025-07-25` |
| `latestFundingDateRange[max]` | date | no | The latest date when the company received its most recent funding round. Use this parameter in combination with `latest_funding_date_range[min]` to set a date range for when the company received its most recent funding round. Example: `2025-09-25` |
| `qOrganizationJobTitles[]` | array<string> | no | The job titles that are listed in active job postings at the company. Examples: `sales manager`; `research analyst` |
| `organizationJobLocations[]` | array<string> | no | The locations of the jobs being actively recruited by the company. Examples: `atlanta`; `japan` |
| `organizationNumJobsRange[min]` | number | no | The minimum number of job postings active at the company. Use this parameter in combination with `organization_num_jobs_range[max]` to set a job postings range. Examples: `50`; `500` |
| `organizationNumJobsRange[max]` | number | no | The maximum number of job postings active at the company. Use this parameter in combination with `organization_num_jobs_range[min]` to set a job postings range. Examples: `50`; `500` |
| `organizationJobPostedAtRange[min]` | date | no | The earliest date when jobs were posted by the company. Use this parameter in combination with `organization_job_posted_at_range[max]` to set a date range for when jobs posted. Example: `2025-07-25` |
| `organizationJobPostedAtRange[max]` | date | no | The latest date when jobs were posted by the company. Use this parameter in combination with `organization_job_posted_at_range[min]` to set a date range for when jobs posted. Example: `2025-09-25` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "breadcrumbs": [
        {
          "displayName": "Ava Chen",
          "label": "string",
          "signalFieldName": "Ava Chen",
          "value": "string"
        }
      ],
      "derivedParams": {
        "recommendationConfigId": "string"
      },
      "disableEuProspecting": true,
      "hasJoin": true,
      "modelIds": [
        "string"
      ],
      "numFetchResult": {},
      "organizations": [
        {
          "alexaRanking": 1,
          "angellistUrl": {},
          "blogUrl": {},
          "crunchbaseUrl": {},
          "facebookUrl": {},
          "foundedYear": 1,
          "hasIntentSignalAccount": true,
          "id": "string",
          "intentSignalAccount": {},
          "intentStrength": {},
          "languages": [
            "string"
          ],
          "linkedinUid": "https://example.com",
          "linkedinUrl": "https://example.com",
          "logoUrl": "https://example.com",
          "naicsCodes": [
            "string"
          ],
          "name": "Ava Chen",
          "organizationHeadcountSixMonthGrowth": 1,
          "organizationHeadcountTwelveMonthGrowth": 1,
          "organizationHeadcountTwentyFourMonthGrowth": 1,
          "organizationRevenue": 1,
          "organizationRevenuePrinted": {},
          "ownedByOrganizationId": {},
          "phone": "string",
          "primaryDomain": "string",
          "primaryPhone": {
            "number": "string",
            "sanitizedNumber": "string",
            "source": "string"
          },
          "publiclyTradedExchange": {},
          "publiclyTradedSymbol": {},
          "sanitizedPhone": "string",
          "showIntent": true,
          "sicCodes": [
            "string"
          ],
          "twitterUrl": "https://example.com",
          "websiteUrl": "https://example.com"
        }
      ],
      "pagination": {
        "page": 1,
        "perPage": 1,
        "totalEntries": 1,
        "totalPages": 1
      },
      "partialResultsLimit": 1,
      "partialResultsOnly": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breadcrumbs[].displayName` | string |  |
| `breadcrumbs[].label` | string |  |
| `breadcrumbs[].signalFieldName` | string |  |
| `breadcrumbs[].value` | string |  |
| `derivedParams.recommendationConfigId` | string |  |
| `disableEuProspecting` | boolean |  |
| `hasJoin` | boolean |  |
| `modelIds[]` | string |  |
| `numFetchResult` | object |  |
| `organizations[].alexaRanking` | number |  |
| `organizations[].angellistUrl` | object |  |
| `organizations[].blogUrl` | object |  |
| `organizations[].crunchbaseUrl` | object |  |
| `organizations[].facebookUrl` | object |  |
| `organizations[].foundedYear` | number |  |
| `organizations[].hasIntentSignalAccount` | boolean |  |
| `organizations[].id` | string |  |
| `organizations[].intentSignalAccount` | object |  |
| `organizations[].intentStrength` | object |  |
| `organizations[].languages[]` | string |  |
| `organizations[].linkedinUid` | string |  |
| `organizations[].linkedinUrl` | string |  |
| `organizations[].logoUrl` | string |  |
| `organizations[].naicsCodes[]` | string |  |
| `organizations[].name` | string |  |
| `organizations[].organizationHeadcountSixMonthGrowth` | number |  |
| `organizations[].organizationHeadcountTwelveMonthGrowth` | number |  |
| `organizations[].organizationHeadcountTwentyFourMonthGrowth` | number |  |
| `organizations[].organizationRevenue` | number |  |
| `organizations[].organizationRevenuePrinted` | object |  |
| `organizations[].ownedByOrganizationId` | object |  |
| `organizations[].phone` | string |  |
| `organizations[].primaryDomain` | string |  |
| `organizations[].primaryPhone.number` | string |  |
| `organizations[].primaryPhone.sanitizedNumber` | string |  |
| `organizations[].primaryPhone.source` | string |  |
| `organizations[].publiclyTradedExchange` | object |  |
| `organizations[].publiclyTradedSymbol` | object |  |
| `organizations[].sanitizedPhone` | string |  |
| `organizations[].showIntent` | boolean |  |
| `organizations[].sicCodes[]` | string |  |
| `organizations[].twitterUrl` | string |  |
| `organizations[].websiteUrl` | string |  |
| `pagination.page` | number |  |
| `pagination.perPage` | number |  |
| `pagination.totalEntries` | number |  |
| `pagination.totalPages` | number |  |
| `partialResultsLimit` | number |  |
| `partialResultsOnly` | boolean |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/mixed_companies/search` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/organization-search.md) for the provider-specific parameters and requirements.

