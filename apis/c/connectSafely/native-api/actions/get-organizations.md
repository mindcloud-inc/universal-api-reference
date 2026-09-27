# Get user organizations with ConnectSafely

Fetch all LinkedIn organizations (company pages) the authenticated user has admin or posting access to. Returns organization details including URN, name, logo, follower count, and visitor count. Use the organization URN for posting content as a company or commenting as a company page.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get user organizations](https://connectsafely.ai/docs/api/linkedin-user/get-organizations-get-organizations)

## Parameters

This endpoint takes no parameters.

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the request was successful |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `organizations` | `array` |  |
| `organizations[].entityUrn` | `string` | Organization URN (e.g., "urn:li:fsd_company:105672170") |
| `organizations[].name` | `string` | Company/organization name |
| `organizations[].universalName` | `string` | URL slug/universal name (e.g., "connectsafelyai") |
| `organizations[].logoUrl` | `string` | Company logo URL (200x200) |
| `organizations[].coverImageUrl` | `string` | Company cover/banner image URL |
| `organizations[].followerCount` | `number` | Number of followers |
| `organizations[].visitorsCount` | `number` | Number of recent visitors |
| `organizations[].pageType` | `string` | Page type (e.g., "COMPANY") |
| `organizations[].isFollowing` | `boolean` | Whether the authenticated user follows this organization |
| `count` | `number` | Total number of organizations returned |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "organizations": [
    {
      "entityUrn": "urn:li:fsd_company:105672170",
      "name": "ConnectSafely.AI",
      "universalName": "connectsafelyai",
      "logoUrl": "https://media.licdn.com/dms/image/v2/D560BAQExfwnRu-WH9g/company-logo_200_200/...",
      "coverImageUrl": "https://media.licdn.com/dms/image/v2/D4D3DAQEZladqoLpujg/image-scale_191_1128/...",
      "followerCount": 1823,
      "visitorsCount": 500,
      "pageType": "COMPANY",
      "isFollowing": true
    },
    {
      "entityUrn": "urn:li:fsd_company:102246628",
      "name": "DCoderAI",
      "universalName": "dcoderai",
      "logoUrl": "https://media.licdn.com/dms/image/v2/D560BAQG68RrbqHxeZA/company-logo_200_200/...",
      "coverImageUrl": "https://media.licdn.com/dms/image/v2/D563DAQGhK5ci_zeTog/image-scale_191_1128/...",
      "followerCount": 213,
      "visitorsCount": 21,
      "pageType": "COMPANY",
      "isFollowing": true
    }
  ],
  "count": 2
}
```

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
