# Search LinkedIn people (alias) with ConnectSafely

Alias endpoint for /search/people. Search for LinkedIn members/professionals with extensive filtering options. Ideal for recruiting, sales prospecting, and networking. Filter by name, job title, company, location, connection degree, and more.

**Recommended:** For `connectionOf` or `followerOf` filters, prefer `search-people-v2` which natively supports these filters and returns more accurate results.

## Endpoint

- **Method:** `POST`
- **Path:** `/people/search`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search LinkedIn people (alias)](https://connectsafely.ai/docs/api/linkedin-search/post-people-search-search-people-alias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use for the search. If not provided, uses the default account. |
| `keywords` | body | `string` | no | Search keywords for name, title, company, or skills Default: ``. |
| `count` | body | `number` | no | Number of results to return per page Default: `25`. |
| `start` | body | `number` | no | Pagination offset (0-indexed) Default: `0`. |
| `filters` | body | `object` | no | Optional filters to narrow down search results |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `people` | `array` |  |
| `people[].profileId` | `string` | LinkedIn profile vanity URL slug (the part after linkedin.com/in/) |
| `people[].profileUrn` | `string` | LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f...") |
| `people[].firstName` | `string` | First name |
| `people[].lastName` | `string` | Last name |
| `people[].headline` | `string` | Profile headline (usually job title and company) |
| `people[].profilePicture` | `string` | URL to profile picture |
| `people[].location` | `string` | Location (city, region, or country) |
| `people[].connectionDegree` | `string` | Connection degree: "1st", "2nd", "3rd+" |
| `people[].currentPosition` | `string` | Current job position text |
| `people[].profileUrl` | `string` | Direct URL to profile |
| `people[].isPremium` | `boolean` | Whether the user has LinkedIn Premium |
| `people[].isOpenToWork` | `boolean` | Whether the user has Open to Work status |
| `totalResults` | `number` |  |
