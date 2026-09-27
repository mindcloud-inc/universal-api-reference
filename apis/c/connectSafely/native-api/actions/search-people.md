# Search LinkedIn people with ConnectSafely

Search for LinkedIn members/professionals with extensive filtering options. Ideal for recruiting, sales prospecting, and networking. Filter by name, job title, company, location, connection degree, and more.

Supports Sales Navigator search URLs — pass a Sales Navigator search URL in the `url` field to use Sales Navigator Lead Search instead of regular LinkedIn search.

### Filtering by location

Two steps: look the location up with `POST /search/geo`, then pass the returned `geoId` as `filters.locationId`.

1. `POST /search/geo` with `{ "keywords": "Ohio" }` returns `{ "geoId": "106981407", "name": "Ohio, United States" }`.
2. `POST /search/people` with that id:

```json
{
  "accountId": "<your-account-id>",
  "keywords": "Mechanical",
  "count": 10,
  "filters": { "locationId": "106981407" }
}
```

Notes:
- Use `filters.locationId` (or its alias `filters.geoUrn`) — there is **no** `filters.location` key. Unknown filter keys are silently ignored and the search runs unfiltered (global results).
- Pass the plain numeric `geoId`. The `urn:li:fsd_geo:<id>` form is also accepted and normalized.
- Any geo level works: country, state, metro area, county, or city. A narrower id gives a narrower result set.
- Location filtering composes with `title`, `industry`, `connectionDegree` and pagination (`start`).

**Recommended:** For `connectionOf` or `followerOf` filters, prefer `search-people-v2` which natively supports these filters and returns more accurate results.

**Rate limit:** 1,000 search calls per account per day (resets at midnight UTC), and 30 calls per minute. Pagination is billed per page walked, so a `count` of 25 spends about 3 calls.

Separately, LinkedIn applies its own **commercial use limit** to people search: roughly 100 searches a month on a free account, ~300 on Premium Career, ~500 on Premium Business, and effectively unlimited with Sales Navigator. That ceiling belongs to LinkedIn, is computed from search and browsing history rather than published, resets on the 1st of the month, and is **not** enforced or reported by this API. Maximum 1000 results per search.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/people`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search LinkedIn people](https://connectsafely.ai/docs/api/linkedin-search/post-search-people-search-people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use for the search. If not provided, uses the default account. |
| `keywords` | body | `string` | no | Search keywords for name, title, company, or skills Default: ``. |
| `count` | body | `number` | no | Number of results to return per page Default: `25`. |
| `start` | body | `number` | no | Pagination offset (0-indexed) Default: `0`. |
| `url` | body | `string` | no | Sales Navigator search URL. When provided, the search will use Sales Navigator Lead Search instead of regular LinkedIn search. The URL should contain `/sales/search/` path (e.g., https://www.linkedin.com/sales/search/people?query=...). |
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
| `pagination` | `object` | Pagination for people search.  `total` is **absent for a normal keyword search**: LinkedIn reports no result count for it, so any total would be invented. Use `hasMore` instead — it is exact, derived by fetching one row past the requested `count`.  `total` **is** returned when searching by a Sales Navigator `url`, because Sales Navigator reports a real result count. Treat it as optional. |
| `pagination.count` | `number` | Number of results returned in this response |
| `pagination.start` | `number` | Starting offset of results |
| `pagination.total` | `number` | Total matching results. Only present for Sales Navigator URL searches — omitted for normal keyword searches, where LinkedIn provides no count. |
| `hasMore` | `boolean` | Whether more results are available past this batch. Derived by fetching one row beyond the requested `count`, so it is exact — not a guess from the page being full. |

### Example response

```json
{
  "success": true,
  "people": [
    {
      "profileId": "abhishek-onkar",
      "profileUrn": "urn:li:fsd_profile:ACoAABdttMcBYTOrkGpTYrhL6waE6Tu8UhpZdeo",
      "firstName": "Abhishek",
      "lastName": "Onkar",
      "headline": "Software Engineer @ Google",
      "profilePicture": "https://media.licdn.com/dms/image/.../profile-displayphoto",
      "location": "Bengaluru",
      "connectionDegree": "2nd",
      "currentPosition": "Software Engineer @ Google",
      "profileUrl": "https://www.linkedin.com/in/abhishek-onkar/",
      "isPremium": false,
      "isOpenToWork": false
    },
    {
      "profileId": "sheetal-lalwani-0601",
      "profileUrn": "urn:li:fsd_profile:ACoAAC11JdABZvl_riyT7he7WnF3OXXr6THQ274",
      "firstName": "Sheetal",
      "lastName": "Lalwani",
      "headline": "Software Engineer at Microsoft",
      "profilePicture": "https://media.licdn.com/dms/image/.../profile-displayphoto",
      "location": "India",
      "connectionDegree": "2nd",
      "currentPosition": "Software Engineer at Microsoft",
      "profileUrl": "https://www.linkedin.com/in/sheetal-lalwani-0601/",
      "isPremium": false,
      "isOpenToWork": false
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
