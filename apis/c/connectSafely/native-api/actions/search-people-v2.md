# Search LinkedIn people (V2 - with auto-pagination) with ConnectSafely

Search for LinkedIn members with enhanced filtering options and automatic pagination. Supports additional filters like connectionOf, followerOf, and schoolIds. Automatically handles LinkedIn page-based pagination internally - specify the total count you want and the API will fetch multiple pages as needed (max 10 pages, ~10 results per page). Better for finding people connected to specific profiles or following specific accounts.

**Important:** This V2 endpoint uses LinkedIn's newer search, which is rolling out gradually by region. If this endpoint does not return results for your account, use the V1 `/search/people` endpoint instead.

**Rate limit:** 1,000 search calls per account per day (resets at midnight UTC), and 30 calls per minute. Pagination is billed per page walked, so a `count` of 25 spends about 3 calls.

Separately, LinkedIn applies its own **commercial use limit** to people search: roughly 100 searches a month on a free account, ~300 on Premium Career, ~500 on Premium Business, and effectively unlimited with Sales Navigator. That ceiling belongs to LinkedIn, is computed from search and browsing history rather than published, resets on the 1st of the month, and is **not** enforced or reported by this API. Maximum 1000 results per search.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/people/v2`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search LinkedIn people (V2 - with auto-pagination)](https://connectsafely.ai/docs/api/linkedin-search/post-search-people-v2-search-people-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `keywords` | body | `string` | no | Search keywords for name, title, company, or skills Default: ``. |
| `count` | body | `number` | no | Total number of results to return. API will automatically paginate through LinkedIn pages (each page ~10 results) to collect this many. Default: `25`. |
| `start` | body | `number` | no | Starting offset (0-indexed). Used to calculate which page to start from. Default: `0`. |
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
| `count` | `number` | Number of people returned in this response |
| `totalCount` | `number` | Total number of matching results available on LinkedIn (may be 0 if unknown) |

### Example response

```json
{
  "success": true,
  "people": [
    {
      "profileId": "shaarifalam",
      "profileUrn": "urn:li:fsd_profile:ACoAACVNMaoBXNhxhJNadDzmfn6cX1bbEa8DFZI",
      "firstName": "Shaarif",
      "lastName": "Alam",
      "headline": "Google Certified UI UX Designer",
      "profilePicture": "https://media.licdn.com/dms/image/.../profile-displayphoto",
      "location": "Delhi, India",
      "connectionDegree": "2nd",
      "profileUrl": "https://www.linkedin.com/in/shaarifalam/",
      "isPremium": false,
      "isOpenToWork": false
    }
  ],
  "count": 3,
  "totalCount": 0
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
