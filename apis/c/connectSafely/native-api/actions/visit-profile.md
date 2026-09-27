# Visit a LinkedIn profile with ConnectSafely

Simulates visiting a LinkedIn profile to trigger the "Who Viewed Your Profile" notification for the target user. This sends the necessary telemetry events that LinkedIn uses to track profile views.

## Endpoint

- **Method:** `POST`
- **Path:** `/profile/visit`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Visit a LinkedIn profile](https://connectsafely.ai/docs/api/linkedin-profiles/post-profile-visit-visit-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | body | `string` | yes | LinkedIn profile vanity URL slug of the user to visit (the part after linkedin.com/in/, e.g., "john-doe-123") |
| `accountId` | body | `string` | no | LinkedIn account ID to use for the visit. If not provided, uses the default account. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the profile visit was successful |
| `profileId` | `string` | The profile ID that was visited |
| `profileUrn` | `string` | The extracted profile URN (ACoAA format) |
| `numericMemberId` | `number` | The numeric member ID extracted from the profile URN |
| `message` | `string` | Success or status message |
| `accountId` | `string` | LinkedIn account ID that performed the visit |

### Example response

```json
{
  "success": true,
  "profileId": "john-doe-123",
  "profileUrn": "ACoAAF7lRPsBwzO9AMvoBVVioq4MmyJUyfiXEqY",
  "numericMemberId": 1592083707,
  "message": "Profile visit registered successfully",
  "accountId": "696ce9e780e0483585e4e553"
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
