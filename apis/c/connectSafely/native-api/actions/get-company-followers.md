# Get company/organization followers with ConnectSafely

Fetch followers of a LinkedIn company page. Returns profile information for each follower including name, headline, profile picture, connection degree, and follow date. Requires admin access to the company page. Use the companyId from the organization URN (e.g., 105672170 from urn:li:fsd_company:105672170).

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:companyId/followers`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get company/organization followers](https://connectsafely.ai/docs/api/linkedin-profiles/get-organizations-companyid-followers-get-company-followers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | param | `string` | yes | LinkedIn company ID (numeric ID from organization URN) |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `start` | query | `number` | no | Pagination offset (0-indexed) Default: `0`. |
| `count` | query | `number` | no | Number of followers to return per page (max 100) Default: `10`. |
| `followerType` | query | `list` | no | Type of followers to retrieve: MEMBER (people) or PAGE (company pages) Accepted values: `MEMBER`, `PAGE`. Default: `MEMBER`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the request was successful |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `companyId` | `string` | The company ID that was queried |
| `followers` | `array` |  |
| `followers[].profileUrn` | `string` | LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAAB...") |
| `followers[].publicIdentifier` | `string` | LinkedIn public identifier / vanity URL (e.g., "john-doe-123") |
| `followers[].firstName` | `string` | Follower first name |
| `followers[].lastName` | `string` | Follower last name |
| `followers[].headline` | `string` | Professional headline |
| `followers[].profilePictureUrl` | `string` | URL to profile picture |
| `followers[].connectionDegree` | `string` | Connection degree (e.g., "DISTANCE_2", "DISTANCE_3") |
| `followers[].followDate` | `string` | Human-readable follow date (e.g., "February 2026") |
| `paging` | `object` |  |
| `paging.start` | `number` | Current pagination offset |
| `paging.count` | `number` | Number of results returned |
| `paging.total` | `number` | Total number of followers (if available) |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "companyId": "105672170",
  "followers": [
    {
      "profileUrn": "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f...",
      "publicIdentifier": "john-doe-123",
      "firstName": "John",
      "lastName": "Doe",
      "headline": "Software Engineer at Tech Company",
      "profilePictureUrl": "https://media.licdn.com/dms/image/v2/...",
      "connectionDegree": "DISTANCE_2",
      "followDate": "February 2026"
    },
    {
      "profileUrn": "urn:li:fsd_profile:ACoAABJefVoBrz3XY4g...",
      "publicIdentifier": "jane-smith-456",
      "firstName": "Jane",
      "lastName": "Smith",
      "headline": "Product Manager | B2B SaaS",
      "profilePictureUrl": "https://media.licdn.com/dms/image/v2/...",
      "connectionDegree": "DISTANCE_3",
      "followDate": "February 2026"
    }
  ],
  "paging": {
    "start": 0,
    "count": 10,
    "total": 1823
  }
}
```

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
