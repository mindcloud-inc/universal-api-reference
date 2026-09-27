# Send a connection request with ConnectSafely

Send a connection request to a LinkedIn member to become 1st-degree connections. Optionally include a personalized message (300 character limit). Connection requests with custom messages have higher acceptance rates. **Either profileId or profileUrn must be provided.** **Rate limit: 90 connection requests per week per LinkedIn account (resets every Monday at midnight UTC). Exceeding the limit puts the account on hold for 24 hours.**

## Endpoint

- **Method:** `POST`
- **Path:** `/connect`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send a connection request](https://connectsafely.ai/docs/api/linkedin-actions/post-connect-send-connection-request)

## Quota

90 connection requests per week per LinkedIn account (resets every Monday at midnight UTC).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `profileId` | body | `string` | no | Target LinkedIn profile vanity URL slug (e.g., "john-doe-123"). Either this or profileUrn is required. Prefer profileUrn when available. |
| `profileUrn` | body | `string` | no | Target LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Either this or profileId is required. Preferred over profileId. |
| `customMessage` | body | `string` | no | Personalized connection message (max 300 characters). Leave empty for default request. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` | Status message |
| `profileUrn` | `string` | LinkedIn URN of the target profile |

### Example response

```json
{
  "success": true,
  "message": "Connection request sent successfully",
  "profileUrn": "urn:li:fsd_profile:ACoAAA24A-MBVEvT49xpVF2gnWrhvmUIPDJshSM"
}
```

## Error status codes

`400`, `401`, `404`, `429`. Bodies follow the shared `{ success, code, message }` error shape.
