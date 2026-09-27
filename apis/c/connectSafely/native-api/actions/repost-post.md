# Repost a LinkedIn post with ConnectSafely

Repost/share a LinkedIn post to your feed. This creates an instant repost without additional commentary. Requires either a post URL (will be scraped for URNs) or the share/ugcPost URN directly. The activityUrn is optional but helps with engagement tracking. Provide companyUrn to repost as a company page you administer instead of your personal profile.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/repost`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Repost a LinkedIn post](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-repost-repost-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `postUrl` | body | `string` | no | Full URL of the LinkedIn post to repost. Will be scraped to extract URNs. |
| `shareUrn` | body | `string` | no | Share URN of the post (e.g., "urn:li:share:7416350085304987648"). Use if you already have the URN. |
| `ugcPostUrn` | body | `string` | no | UGC Post URN (e.g., "urn:li:ugcPost:7417595827650519041"). Used as fallback if shareUrn not available. |
| `activityUrn` | body | `string` | no | Activity URN for pre-repost signal (e.g., "urn:li:activity:7416350088379338752"). Optional but recommended. |
| `companyUrn` | body | `string` | no | Optional. Repost as a company page you administer instead of your personal profile. Provide the company URN (e.g., "urn:li:fsd_company:134684122"). |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `repostUrn` | `string` | URN of the created repost |
| `repostUrl` | `string` | Viewable permalink of the created repost (LinkedIn's "View repost" link). May be absent if LinkedIn returns no toast link. |
| `resourceKey` | `string` | Resource key of the repost |
| `shareUrn` | `string` | Share URN that was reposted |
| `ugcPostUrn` | `string` | UGC Post URN that was reposted (if shareUrn not available) |
| `activityUrn` | `string` | Activity URN used for tracking |
| `accountId` | `string` | LinkedIn account ID that performed the repost |
| `companyUrn` | `string` | Company URN the repost was authored as (only present when reposting as a company page) |

### Example response

```json
{
  "success": true,
  "message": "Repost successful",
  "repostUrn": "urn:li:fsd_repost:urn:li:instantRepost:(urn:li:share:7430667225633550337,7432008152021254154)",
  "repostUrl": "https://www.linkedin.com/feed/update/urn:li:activity:7432008152089161728",
  "resourceKey": "urn:li:fsd_repost:urn:li:instantRepost:(urn:li:share:7430667225633550337,7432008152021254154)",
  "shareUrn": "urn:li:share:7430667225633550337",
  "activityUrn": "urn:li:activity:7430667226199830528",
  "accountId": "696ce9e780e0483585e4e553",
  "companyUrn": "urn:li:fsd_company:134684122"
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
