# Search LinkedIn groups with ConnectSafely

Search for LinkedIn groups by keywords. Groups are communities where professionals discuss industry topics, share insights, and network.

LinkedIn's group search offers a keyword box and nothing else — there are **no filters** — so `filters.memberCount` is accepted for backward compatibility but never applied; sort/filter the returned `memberCount` client-side instead.

Results are paged internally to satisfy `count`. Page sizes vary (8-10 rows), so a short page is not the end of the result set — use `hasMore`, never the length of the returned array, to decide whether to keep paging.

**Rate limit:** no per-account search quota is enforced on this endpoint — only the general 30-calls-per-minute velocity limit.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/groups`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search LinkedIn groups](https://connectsafely.ai/docs/api/linkedin-search/post-search-groups-search-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use for the search. If not provided, uses the default account. |
| `keywords` | body | `string` | no | Search keywords for group name or description Default: ``. |
| `count` | body | `number` | no | Number of results to return per page Default: `25`. |
| `start` | body | `number` | no | Pagination offset (0-indexed) Default: `0`. |
| `filters` | body | `object` | no | Optional filters to narrow down search results |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `groups` | `array` |  |
| `groups[].groupId` | `string` | Unique LinkedIn group ID |
| `groups[].name` | `string` | Group name |
| `groups[].memberCount` | `number` | Members in the group. LinkedIn rounds this on the search screen — anything past ~999 comes back as the displayed approximation (`1K members` → `1000`, `89K members` → `89000`). Counts below 1000 are exact. Fetch the group with `get-group-details` for a precise figure. |
| `groups[].logoUrl` | `string` | URL to group logo/image |
| `groups[].groupUrl` | `string` | Direct URL to group page |
| `groups[].isPrivate` | `boolean` | Whether the group requires approval to join |
| `pagination` | `object` | Pagination for group search.  `total` is LinkedIn's own result count for the query, and is **optional** — most queries report one, but some render none and a zero-result query never does. Treat it as approximate for large result sets: LinkedIn displays exact counts for small ones ("580 results") and rounded ones for big ones ("About 90,000 results"), and both arrive here as a plain number.  `hasMore` is always present and is the field to page on. |
| `pagination.count` | `number` | Number of results returned in this response |
| `pagination.start` | `number` | Starting offset of results |
| `pagination.total` | `number` | LinkedIn's reported result count for this query. Omitted when LinkedIn renders no count. Approximate for large result sets. |
| `hasMore` | `boolean` | Whether more results are available past this batch. Derived by fetching one row beyond the requested `count`, so it is exact — not a guess from the page being full. |

### Example response

```json
{
  "success": true,
  "groups": [
    {
      "groupId": "9121382",
      "name": "AI & GTM (News, Jobs, Tools and everything in between)",
      "memberCount": 1000,
      "logoUrl": "https://media.licdn.com/dms/image/.../group-logo",
      "groupUrl": "https://www.linkedin.com/groups/9121382/",
      "isPrivate": false
    },
    {
      "groupId": "8645802",
      "name": "GTM AI",
      "memberCount": 813,
      "logoUrl": "https://media.licdn.com/dms/image/.../group-logo",
      "groupUrl": "https://www.linkedin.com/groups/8645802/",
      "isPrivate": true
    }
  ],
  "pagination": {
    "count": 10,
    "start": 0,
    "total": 580
  },
  "hasMore": true
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
