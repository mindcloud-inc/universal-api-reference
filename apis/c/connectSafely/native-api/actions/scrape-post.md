# Scrape LinkedIn post details with ConnectSafely

Extract detailed information from a LinkedIn post URL including content, author, engagement metrics, and media. Uses caching to reduce API calls. Supports both authenticated and public scraping with proxy rotation for reliability. Use forceRefresh to bypass cache.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/scrape`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Scrape LinkedIn post details](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-scrape-scrape-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postUrl` | body | `string` | yes | Full LinkedIn post URL to scrape |
| `accountId` | body | `string` | no | LinkedIn account ID for authenticated scraping (gets more data than public) |
| `useCache` | body | `boolean` | no | Whether to use cached results if available Default: `True`. |
| `maxCacheAge` | body | `number` | no | Maximum age of cached data in hours before refresh Default: `24`. |
| `maxProxyRetries` | body | `number` | no | Number of proxy rotation attempts on failure Default: `3`. |
| `forceRefresh` | body | `boolean` | no | Force fresh scrape ignoring cache Default: `False`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` | Whether the scrape was successful |
| `originalUrl` | `string` | Original URL provided in the request |
| `finalUrl` | `string` | Final URL after any redirects |
| `scrapeDuration` | `number` | Time taken to scrape in milliseconds |
| `data` | `object` | Scraped post data |
| `data.content` | `string` | Full text content of the post |
| `data.ugcPostUrn` | `string` | UGC Post URN identifier |
| `data.activityUrn` | `string` | Activity URN identifier |
| `data.shareUrn` | `string` | Share URN if available |
| `data.featuredActivityUrn` | `string` | Featured activity URN if applicable |
| `data.author` | `object` |  |
| `data.author.name` | `string` | Author display name |
| `data.author.headline` | `string` | Author headline/title |
| `data.author.profileUrl` | `string` | URL to author LinkedIn profile |
| `data.timestamp` | `string` | Post timestamp (relative or absolute) |
| `data.engagement` | `object` |  |
| `data.engagement.likes` | `number` | Number of likes/reactions |
| `data.engagement.comments` | `number` | Number of comments |
| `data.engagement.shares` | `number` | Number of shares/reposts |
| `data.media` | `object` | Media types present in the post |
| `data.media.hasImages` | `boolean` |  |
| `data.media.hasVideo` | `boolean` |  |
| `data.media.hasDocument` | `boolean` |  |
| `data.media.hasArticle` | `boolean` |  |
| `data.media.hasLink` | `boolean` |  |
| `data.media.hasPoll` | `boolean` |  |
| `data.permissions` | `object` |  |
| `data.permissions.canComment` | `boolean` | Whether the authenticated account can comment on this post. false when the post restricts commenting (e.g. "Only connections can comment on this post" and the account is not a connection) or commenting is fully disabled. Accurate only with authenticated scraping; defaults to true otherwise. |
| `data.url` | `string` | Canonical post URL |
| `data.scraped` | `boolean` | Indicates data was scraped |
| `data.scrapedAt` | `date` | Timestamp when post was scraped |
| `usingAuthenticatedScraping` | `boolean` | Whether authenticated scraping was used |
| `message` | `string` | Success message |

### Example response

```json
{
  "success": true,
  "originalUrl": "https://www.linkedin.com/posts/john-doe-123_example-post-activity-7430667226199830528-Cu89",
  "finalUrl": "https://www.linkedin.com/posts/john-doe-123_example-post-activity-7430667226199830528-Cu89",
  "scrapeDuration": 4092,
  "data": {
    "content": "This is an example post content with insights about technology and business...",
    "ugcPostUrn": "urn:li:ugcPost:7430667225633550337",
    "activityUrn": "urn:li:activity:7430667226199830528",
    "shareUrn": null,
    "featuredActivityUrn": null,
    "author": {
      "name": "John Doe",
      "headline": "Software Engineer at Tech Company",
      "profileUrl": "https://www.linkedin.com/in/john-doe-123"
    },
    "timestamp": "2d",
    "engagement": {
      "likes": 86,
      "comments": 12,
      "shares": 3
    },
    "media": {
      "hasImages": true,
      "hasVideo": false,
      "hasDocument": false,
      "hasArticle": false,
      "hasLink": true,
      "hasPoll": false
    },
    "permissions": {
      "canComment": true
    },
    "url": "https://www.linkedin.com/posts/john-doe-123_example-post-activity-7430667226199830528-Cu89",
    "scraped": true,
    "scrapedAt": "2026-02-24 12:56:58.220000+00:00"
  },
  "usingAuthenticatedScraping": true,
  "message": "Successfully scraped post content"
}
```

## Error status codes

`400`, `401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
