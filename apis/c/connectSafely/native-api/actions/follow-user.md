# Follow or unfollow a LinkedIn profile with ConnectSafely

Follow or unfollow a LinkedIn member to see their posts in your feed. Following does not require a connection. Provide either profileId (public identifier) or profileUrn (internal URN). Following builds your network visibility without sending connection requests. **Rate limit: 100 actions per day.**

## Endpoint

- **Method:** `POST`
- **Path:** `/follow`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Follow or unfollow a LinkedIn profile](https://connectsafely.ai/docs/api/linkedin-actions/post-follow-follow-user)

## Quota

100 follow/unfollow actions per day per LinkedIn account (not per API key).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `profileId` | body | `string` | no | LinkedIn profile vanity URL slug (the part after linkedin.com/in/, e.g., "john-doe-123"). Prefer profileUrn when available. |
| `profileUrn` | body | `string` | no | LinkedIn profile URN (e.g., "urn:li:fsd_profile:ACoAABJefVoBrz2LR3f..."). Preferred over profileId. |
| `action` | body | `list` | no | Action to perform: follow or unfollow the profile Accepted values: `follow`, `unfollow`. Default: `follow`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `action` | `list` |  |
| `profileUrn` | `string` | LinkedIn profile URN of the followed/unfollowed user |
| `message` | `string` |  |

### Example response

```json
{
  "success": true,
  "action": "follow",
  "profileUrn": "urn:li:fsd_profile:ACoAAA24A-MBVEvT49xpVF2gnWrhvmUIPDJshSM",
  "message": "Successfully followed user"
}
```

## Error status codes

`400`, `401`, `404`, `429`. Bodies follow the shared `{ success, code, message }` error shape.
