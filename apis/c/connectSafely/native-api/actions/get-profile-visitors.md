# Get profile visitors with ConnectSafely

Retrieve a list of people who viewed your LinkedIn profile. Shows visitor name, headline, location, and visit timestamp. Some visitors may be anonymous depending on their privacy settings. Supports pagination and various time ranges.

## Endpoint

- **Method:** `POST`
- **Path:** `/profile/visitors`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get profile visitors](https://connectsafely.ai/docs/api/linkedin-user/post-profile-visitors-get-profile-visitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `timeRange` | body | `list` | no | Time range to filter visitors Accepted values: `past_7_days`, `past_30_days`, `past_90_days`, `past_1_year`, `PAST_7_DAYS`, `PAST_30_DAYS`, `PAST_90_DAYS`, `ALL_TIME`. Default: `past_90_days`. |
| `count` | body | `number` | no | Page size for pagination (visitors fetched per API request). Use maxVisitors to control the total limit. Default: `20`. |
| `start` | body | `number` | no | Pagination offset (0-indexed) Default: `0`. |
| `fetchAll` | body | `boolean` | no | When true, automatically paginates to fetch all visitors up to maxVisitors limit Default: `False`. |
| `maxVisitors` | body | `number` | yes | Total number of visitors to retrieve. This is the primary limit - use this parameter to specify how many visitors you want (e.g., maxVisitors: 50 for 50 visitors). Default: `20`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the request was successful |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `visitors` | `array` |  |
| `visitors[].entityUrn` | `string` | Profile URN (e.g., "urn:li:fsd_profile:...") |
| `visitors[].publicIdentifier` | `string` | Profile URL slug (e.g., "john-doe-123") |
| `visitors[].name` | `string` | Full name of the visitor |
| `visitors[].headline` | `string` | Professional headline |
| `visitors[].profilePicture` | `string` | Profile picture URL (100x100 thumbnail) |
| `visitors[].viewedAt` | `string` | Human-readable time since visit (e.g., "Viewed 1h ago", "Viewed 2d ago") |
| `visitors[].connectionDegree` | `string` | Connection degree: "1st", "2nd", "3rd", or "3rd+" |
| `visitors[].profileUrl` | `string` | Full LinkedIn profile URL |
| `pagination` | `object` |  |
| `pagination.start` | `number` | Current offset |
| `pagination.count` | `number` | Number of visitors in this response |
| `pagination.total` | `number` | Total number of visitors available |
| `hasMore` | `boolean` | Whether more visitors are available for pagination |
| `timeRange` | `string` | Time range filter applied |
| `filters` | `object` | Filters applied to the request |
| `filters.timeRange` | `string` |  |
| `filters.count` | `number` |  |
| `filters.start` | `number` |  |
| `filters.fetchAll` | `boolean` |  |
| `filters.maxVisitors` | `number` |  |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "visitors": [
    {
      "entityUrn": "urn:li:fsd_profile:ACoAADlVtYMBLWFFOJ1ezKvVfycTiiAjoFmMK68",
      "publicIdentifier": "ritika-kulkarni-85718922a",
      "name": "Ritika Kulkarni",
      "headline": "Full Stack Developer | Agentic AI | Python | Gen AI",
      "profilePicture": "https://media.licdn.com/dms/image/v2/D4D03AQEi_YdnvAQoew/profile-displayphoto-shrink_100_100/...",
      "viewedAt": "Viewed 47m ago",
      "connectionDegree": "1st",
      "profileUrl": "https://www.linkedin.com/in/ritika-kulkarni-85718922a"
    },
    {
      "entityUrn": "urn:li:fsd_profile:ACoAAFcWhRYB8fzl-VIyjFSFXfhToQE6M5bJiuw",
      "publicIdentifier": "mamta-mishra-386398349",
      "name": "Mamta Mishra",
      "headline": "Student at Dr. Ram Manohar Lohia Awadh University",
      "profilePicture": "https://media.licdn.com/dms/image/v2/D5603AQFdaHjJWpZbww/profile-displayphoto-shrink_100_100/...",
      "viewedAt": "Viewed 52m ago",
      "connectionDegree": "2nd",
      "profileUrl": "https://www.linkedin.com/in/mamta-mishra-386398349"
    }
  ],
  "pagination": {
    "start": 0,
    "count": 10,
    "total": 8
  },
  "hasMore": false,
  "timeRange": null,
  "filters": {
    "timeRange": "past_90_days",
    "count": 20,
    "start": 0,
    "fetchAll": false,
    "maxVisitors": 10
  }
}
```

## Error status codes

`401`, `403`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
