# Search LinkedIn companies with ConnectSafely

Search for companies on LinkedIn by keywords and filters. Filter by headquarters location, industry, and company size. Useful for lead generation, market research, and finding potential business partners.

Handles LinkedIn's page-based pagination internally: ask for the total `count` you want and the API walks as many ~10-result pages as it takes (max 11).

`filters.companyType` and `filters.followedCompanies` are still accepted but **no longer narrow the result set** — LinkedIn's current company search offers no such facet.

**Sales Navigator Support:** Pass a Sales Navigator company search URL in the `url` parameter to search using Sales Navigator filters (revenue, employees, etc.). **Requires Sales Navigator license on the LinkedIn account.**

**Rate limit:** 1,000 search calls per account per day (resets at midnight UTC), and 30 calls per minute. Pagination is billed per page walked, so a `count` of 25 spends about 3 calls.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/companies`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search LinkedIn companies](https://connectsafely.ai/docs/api/linkedin-search/post-search-companies-search-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use for the search. If not provided, uses the default account. |
| `keywords` | body | `string` | no | Search keywords for company name or description (used for regular LinkedIn search) Default: ``. |
| `url` | body | `string` | no | Sales Navigator company search URL (e.g., https://www.linkedin.com/sales/search/company?query=...). **Requires Sales Navigator license.** When provided, uses Sales Navigator API with advanced filters like revenue and employee count. |
| `count` | body | `number` | no | Total number of results to return. Pages are walked internally to reach it — see the rate-limit note. Default: `25`. |
| `start` | body | `number` | no | Row offset to start from (0-indexed). Need not land on a page boundary. Default: `0`. |
| `filters` | body | `object` | no | Optional filters to narrow down search results |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `companies` | `array` |  |
| `companies[].companyId` | `string` | Unique LinkedIn company ID |
| `companies[].name` | `string` | Company name |
| `companies[].universalName` | `string` | Company URL slug (e.g., "google") |
| `companies[].headline` | `string` | Company headline with industry and location |
| `companies[].description` | `string` | Brief company description |
| `companies[].logoUrl` | `string` | URL to company logo image |
| `companies[].industry` | `string` | Primary industry classification |
| `companies[].followerCount` | `number` | Number of LinkedIn followers |
| `companies[].companyUrl` | `string` | Direct URL to company page |
| `companies[].location` | `string` | Company headquarters location |
| `pagination` | `object` | Pagination for company search.  `total` is **absent for a normal keyword search**: LinkedIn reports no result count for it, so any total would be invented. Use `hasMore` instead — it is derived by fetching one row past the requested `count`.  `total` **is** returned when searching by a Sales Navigator `url`, because Sales Navigator reports a real result count. Treat it as optional. |
| `pagination.count` | `number` | Number of results returned in this response |
| `pagination.start` | `number` | Starting offset of results |
| `pagination.total` | `number` | Total matching results. Only present for Sales Navigator URL searches — omitted for normal keyword searches, where LinkedIn provides no count. |
| `hasMore` | `boolean` | Whether more results are available |

### Example response

```json
{
  "success": true,
  "companies": [
    {
      "companyId": "1441",
      "name": "Google",
      "universalName": "google",
      "headline": "Software Development \u2022 Mountain View, CA",
      "description": "A problem isn't truly solved until it's solved for all.",
      "logoUrl": "https://media.licdn.com/dms/image/.../google_logo",
      "industry": "Software Development",
      "followerCount": 41000000,
      "companyUrl": "https://www.linkedin.com/company/google/",
      "location": "Mountain View, CA"
    },
    {
      "companyId": "1594050",
      "name": "Google DeepMind",
      "universalName": "googledeepmind",
      "headline": "Research Services \u2022 London, London",
      "description": "We're committed to solving intelligence.",
      "logoUrl": "https://media.licdn.com/dms/image/.../googledeepmind_logo",
      "industry": "Research Services",
      "followerCount": 1000000,
      "companyUrl": "https://www.linkedin.com/company/googledeepmind/",
      "location": "London, London"
    }
  ],
  "pagination": {
    "count": 25,
    "start": 0
  },
  "hasMore": true
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
