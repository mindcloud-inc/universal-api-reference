# Check if profile supports email messaging with ConnectSafely

Check whether a LinkedIn profile has email messaging enabled (open profile). Some LinkedIn members allow direct email contact through their profile. Use this to verify before attempting email outreach.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/check-email-support`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Check if profile supports email messaging](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-check-email-support-check-email-support)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `profileId` | body | `string` | no | LinkedIn profile vanity URL slug (e.g., "john-doe-123"). Prefer profileUrn when available. |
| `profileUrn` | body | `string` | no | LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN..."). Preferred over profileId. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` |  |
| `profileId` | `string` |  |
| `profileUrn` | `string` |  |
| `supportsFreeEmail` | `boolean` |  |
| `message` | `string` |  |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "profileId": null,
  "profileUrn": "urn:li:fsd_profile:ACoAAFpqSoMB8vTqRbg4mN_wbabO8w0gjgFu-6o",
  "supportsFreeEmail": true,
  "message": "Profile supports free email messaging (open profile)"
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
