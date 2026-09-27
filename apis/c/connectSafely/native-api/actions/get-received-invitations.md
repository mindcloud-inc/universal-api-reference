# Get received invitations with ConnectSafely

Retrieves received invitations from LinkedIn including connection requests, organization follow invites, and newsletter subscriptions. Returns invitation details with category classification (CONNECTION, ORGANIZATION, NEWSLETTER, EVENT, MEMBER_FOLLOW). Supports pagination via startIndex parameter. **Paginating clients must stop on `endOfList: true`, not on an empty array** — an empty page with HTTP 502 / `code: INVITATIONS_UNAVAILABLE` means LinkedIn temporarily returned nothing while the account still has pending invitations, and the request should be retried.

## Endpoint

- **Method:** `GET`
- **Path:** `/invitations/received`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get received invitations](https://connectsafely.ai/docs/api/linkedin-user/get-invitations-received-get-received-invitations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `startIndex` | query | `number` | no | Pagination start index (0-indexed). Each page returns 10 invitations. Default: `0`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `invitations` | `array` |  |
| `invitations[].id` | `string` | Unique invitation identifier |
| `invitations[].invitationId` | `string` | LinkedIn invitation ID |
| `invitations[].invitationUrn` | `string` | LinkedIn invitation URN |
| `invitations[].memberId` | `string` | LinkedIn member ID. Empty for organization/newsletter invitations. |
| `invitations[].memberUrn` | `string` | LinkedIn member URN (e.g., "urn:li:fsd_profile:ACoAAA..."). Empty for organization/newsletter invitations. |
| `invitations[].invitationType` | `list` | Always RECEIVED |
| `invitations[].invitationCategory` | `list` | Category of the invitation |
| `invitations[].linkedInInvitationType` | `string` | Raw LinkedIn invitation type (e.g., GenericInvitationType_CONNECTION) |
| `invitations[].validationToken` | `string` | Token required for accept/ignore actions |
| `invitations[].receivedAt` | `string` | Relative timestamp (e.g., "2 weeks ago") |
| `invitations[].customMessage` | `string` | Custom message included with the invitation |
| `invitations[].newsletterName` | `string` | Newsletter name (only for NEWSLETTER category) |
| `invitations[].companyName` | `string` | Company name (only for ORGANIZATION/NEWSLETTER categories) |
| `invitations[].profile` | `object` |  |
| `invitations[].profile.firstName` | `string` | First name of the inviter |
| `invitations[].profile.lastName` | `string` | Last name of the inviter |
| `invitations[].profile.profileUrl` | `string` | Full LinkedIn profile URL |
| `invitations[].profile.publicIdentifier` | `string` | LinkedIn public profile identifier |
| `count` | `number` | Number of invitations returned |
| `endOfList` | `boolean` | true only when this page is empty AND the page genuinely contained no invitation cards AND the account has no pending connection requests beyond startIndex. Paginate until this is true — never stop on an empty array alone. |
| `startIndex` | `number` | Current pagination start index |
| `accountId` | `string` | LinkedIn account ID used |

### Example response

```json
{
  "success": true,
  "endOfList": false,
  "invitations": [
    {
      "id": "7455891636745551899",
      "invitationId": "7455891636745551899",
      "invitationUrn": "urn:li:invitation:7455891636745551899",
      "memberId": "",
      "memberUrn": "",
      "invitationType": "RECEIVED",
      "invitationCategory": "ORGANIZATION",
      "linkedInInvitationType": "GenericInvitationType_ORGANIZATION",
      "validationToken": "C712w50Z",
      "receivedAt": "2 weeks ago",
      "companyName": "ZenX8Studio",
      "profile": {
        "firstName": "Yash",
        "lastName": "Jadhav",
        "profileUrl": "https://www.linkedin.com/in/yash-jadhav-a03656326/",
        "publicIdentifier": "yash-jadhav-a03656326"
      }
    },
    {
      "id": "7455163451166860117",
      "invitationId": "7455163451166860117",
      "invitationUrn": "urn:li:invitation:7455163451166860117",
      "memberId": "",
      "memberUrn": "",
      "invitationType": "RECEIVED",
      "invitationCategory": "NEWSLETTER",
      "linkedInInvitationType": "GenericInvitationType_ORGANIZATION",
      "validationToken": "EJx1vfKg",
      "receivedAt": "2 weeks ago",
      "newsletterName": "VAYUZ Insights",
      "profile": {
        "firstName": "Natalya",
        "lastName": "Singh",
        "profileUrl": "",
        "publicIdentifier": ""
      }
    },
    {
      "id": "7455301624689844224",
      "invitationId": "7455301624689844224",
      "invitationUrn": "urn:li:invitation:7455301624689844224",
      "memberId": "ACoAAAYHg8oBNy-PmYu4ZIXcv5yOcNldwpl8lj8",
      "memberUrn": "urn:li:fsd_profile:ACoAAAYHg8oBNy-PmYu4ZIXcv5yOcNldwpl8lj8",
      "invitationType": "RECEIVED",
      "invitationCategory": "CONNECTION",
      "linkedInInvitationType": "GenericInvitationType_CONNECTION",
      "validationToken": "jywembME",
      "receivedAt": "2 weeks ago",
      "profile": {
        "firstName": "Deepika",
        "lastName": "Khare",
        "profileUrl": "https://www.linkedin.com/in/deepika-khare/",
        "publicIdentifier": "deepika-khare"
      }
    }
  ],
  "count": 10,
  "startIndex": 0,
  "accountId": "69da1eacf365891afa0426a4"
}
```

## Error status codes

`401`, `500`, `502`. Bodies follow the shared `{ success, code, message }` error shape.
