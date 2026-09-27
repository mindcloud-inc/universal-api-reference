# Search LinkedIn jobs with ConnectSafely

Search for job postings on LinkedIn with various filters. Supports pagination and multiple filter criteria including location, employment type, experience level, and more.

**Filters changed when LinkedIn rebuilt its job search.** `industry`, `locationId`, `geoUrn` and `jobType` are rejected with a 400 rather than ignored — LinkedIn no longer offers those filters. Use `employmentType`, `experienceLevel`, `geoId`, and `segmentIds` (filter-pill ids, e.g. `"225001:272001"` for Remote).

| Old filter | Use instead |
| --- | --- |
| `jobType: ["F"]` | `employmentType: ["full-time"]` |
| `experienceLevel: ["4","5","6"]` | `experienceLevel: ["senior","director","executive"]` |
| `workplaceType: ["2"]` (Remote) | `workplaceType: ["remote"]` |
| `industry` | `segmentIds` (the ids LinkedIn offers vary by keyword) |
| `locationId` / `geoUrn` | `geoId` |

**`workplaceType` is applied to the returned cards, not by LinkedIn.** LinkedIn honours the Remote segment, but when the fully-filtered pool is thin it BACKFILLS the page with rows that do not match and still answers 200. Measured on one account with keywords "VP of Marketing" and the Remote segment held constant: alone 10/10 remote, plus `experienceLevel` 9/10, plus `past-month` 8/10, plus `past-week` 5/10, plus `past-24h` 5/10, plus `past-24h` and `experienceLevel` 4/10. It tracks how narrow the filter set is, not the keyword, so no segment id avoids it. Filtering on each card's own pill is therefore the only reliable option, with two consequences: a page may return fewer than `count` rows (check `hasMore` and page on), and jobs LinkedIn labels with no workplace pill are excluded rather than assumed.

**Rate limit:** 1,000 search calls per account per day (resets at midnight UTC), and 30 calls per minute. One request counts as one call regardless of `count`.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/jobs`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search LinkedIn jobs](https://connectsafely.ai/docs/api/linkedin-search/post-search-jobs-search-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use for the search. If not provided, uses the default account. |
| `keywords` | body | `string` | no | Search keywords for job title, company, or description Default: ``. |
| `count` | body | `number` | no | Number of results to return per page Default: `25`. |
| `start` | body | `number` | no | Pagination offset (0-indexed) Default: `0`. |
| `filters` | body | `object` | no | Optional filters to narrow down search results |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `jobs` | `array` |  |
| `jobs[].jobId` | `string` | Unique LinkedIn job posting ID |
| `jobs[].title` | `string` | Job title |
| `jobs[].companyName` | `string` | Name of the hiring company |
| `jobs[].companyLogo` | `string` | Company logo URL |
| `jobs[].location` | `string` | Job location, without the work-type suffix (e.g., "Bengaluru, Karnataka, India") |
| `jobs[].isRemote` | `boolean` | Whether the position is fully remote |
| `jobs[].isHybrid` | `boolean` | Whether the position is hybrid (partial remote) |
| `jobs[].postedDate` | `string` | Relative posting age as LinkedIn renders it (e.g., "Posted 4 days ago") |
| `jobs[].salary` | `string` | Pay-rate badge when the posting shows one (e.g., "30K INR/month - 45K INR/month") |
| `jobs[].jobUrl` | `string` | Direct URL to the job posting |
| `jobs[].easyApply` | `boolean` | Whether LinkedIn Easy Apply is available |
| `pagination` | `object` | Pagination for job search.  `total` is **never returned**: LinkedIn reports no result count for job search, so any total would be invented. Unlike people and company search there is no Sales Navigator variant that reports one. Use `hasMore` instead. |
| `pagination.count` | `number` | Number of results returned in this response |
| `pagination.start` | `number` | Starting offset of results |
| `hasMore` | `boolean` | Whether more results are available |

### Example response

```json
{
  "success": true,
  "jobs": [
    {
      "jobId": "4367156030",
      "title": "Founding Software Engineer - AI and Backend",
      "companyName": "Dexicon",
      "companyLogo": "https://media.licdn.com/dms/image/v2/D560BAQ.../company-logo_100_100/...",
      "location": "Bengaluru, Karnataka, India",
      "isRemote": true,
      "isHybrid": false,
      "postedDate": "Posted 4 days ago",
      "jobUrl": "https://www.linkedin.com/jobs/view/4367156030/",
      "easyApply": false
    },
    {
      "jobId": "4321502503",
      "title": "Software Engineer (backend)",
      "companyName": "Kodo",
      "companyLogo": "https://media.licdn.com/dms/image/v2/C4D0BAQ.../company-logo_100_100/...",
      "location": "Mumbai Metropolitan Region",
      "isRemote": false,
      "isHybrid": false,
      "postedDate": "Posted 2 days ago",
      "salary": "30K INR/month - 45K INR/month",
      "jobUrl": "https://www.linkedin.com/jobs/view/4321502503/",
      "easyApply": true
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

`400`, `401`, `429`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
