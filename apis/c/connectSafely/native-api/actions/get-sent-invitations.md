# Get sent connection invitations with ConnectSafely

Retrieves sent connection invitations from LinkedIn. Returns a list of pending invitations with profile information, timestamps, and invitation IDs. Supports pagination via startIndex parameter.

## Endpoint

- **Method:** `GET`
- **Path:** `/invitations/sent`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get sent connection invitations](https://connectsafely.ai/docs/api/linkedin-user/get-invitations-sent-get-sent-invitations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `startIndex` | query | `number` | no | Pagination start index (0-indexed). Use to fetch additional pages of invitations. Default: `0`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `invitations` | `array` |  |
| `invitations[].id` | `string` | Unique invitation identifier |
| `invitations[].invitationId` | `string` | LinkedIn invitation ID |
| `invitations[].invitationUrn` | `string` | LinkedIn invitation URN (e.g., "urn:li:invitation:123456") |
| `invitations[].memberId` | `string` | LinkedIn member ID (ACoAAA format) |
| `invitations[].memberUrn` | `string` | LinkedIn member URN (e.g., "urn:li:fsd_profile:ACoAAA...") |
| `invitations[].invitationType` | `list` | Type of invitation |
| `invitations[].sentAt` | `string` | Relative timestamp (e.g., "2 days ago", "1 week ago") |
| `invitations[].profile` | `object` |  |
| `invitations[].profile.firstName` | `string` | First name of the invited person |
| `invitations[].profile.lastName` | `string` | Last name of the invited person |
| `invitations[].profile.headline` | `string` | Professional headline |
| `invitations[].profile.profileUrl` | `string` | Full LinkedIn profile URL |
| `invitations[].profile.publicIdentifier` | `string` | LinkedIn public profile identifier |
| `count` | `number` | Number of invitations returned |
| `startIndex` | `number` | Current pagination start index |
| `accountId` | `string` | LinkedIn account ID used for the request |

### Example response

```json
{
  "success": true,
  "invitations": [
    {
      "id": "7897046780350316544",
      "invitationId": "7897046780350316544",
      "invitationUrn": "urn:li:invitation:7897046780350316544",
      "memberId": "ACoAADPy0YkBl72yFV0nJCqXd2F9OBxiI7Tvhg4",
      "memberUrn": "urn:li:fsd_profile:ACoAADPy0YkBl72yFV0nJCqXd2F9OBxiI7Tvhg4",
      "invitationType": "SENT",
      "sentAt": "2 days ago",
      "profile": {
        "firstName": "John",
        "lastName": "Doe",
        "headline": "CEO | Entrepreneur | Tech Founder",
        "profileUrl": "https://www.linkedin.com/in/johndoe",
        "publicIdentifier": "johndoe"
      }
    }
  ],
  "count": 10,
  "startIndex": 0,
  "accountId": "696ce9e780e0483585e4e553"
}
```

## Error status codes

`401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
