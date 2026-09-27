# Search posts by keyword with ConnectSafely

Search LinkedIn posts by keywords with filtering options. Find relevant content for engagement, monitor industry discussions, or discover trending topics. Filter by date posted, sort by relevance or recency, and target posts by author job titles.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/search`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Search posts by keyword](https://connectsafely.ai/docs/api/linkedin-posts/post-posts-search-search-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `keywords` | body | `string` | yes | Search keywords to find in post content |
| `count` | body | `number` | no | Number of posts to return per page Default: `50`. |
| `start` | body | `number` | no | Pagination offset (0-indexed) Default: `0`. |
| `datePosted` | body | `list` | no | Filter by when post was published Accepted values: `past-24h`, `past-week`, `past-month`, `any-time`. Default: `any-time`. |
| `sortBy` | body | `list` | no | Sort order: relevance (best match) or date_posted (newest first) Accepted values: `relevance`, `date_posted`. Default: `relevance`. |
| `authorJobTitles` | body | `array` | no | Filter by author job titles (e.g., ["CEO", "VP Marketing"]) |
| `exactSearch` | body | `boolean` | no | When true (default), the keyword is wrapped in double quotes for an exact-phrase match. Set to false for a broader search that also matches individual terms. Default: `True`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `keyword` | `string` |  |
| `accountId` | `string` |  |
| `posts` | `array` |  |
| `posts[].urn` | `string` | Activity URN of the post |
| `posts[].url` | `string` | Permalink of the post |
| `posts[].postUrl` | `string` | Alias of `url` — same value, kept for legacy clients |
| `posts[].text` | `string` |  |
| `posts[].userCommentary` | `string` | Same value as `text` |
| `posts[].content` | `string` | Alias of `text` — same value, kept for legacy clients |
| `posts[].authorName` | `string` | Alias of `author.name` |
| `posts[].authorProfileUrl` | `string` | Alias of `author.profileUrl` |
| `posts[].canComment` | `boolean` | Always true here — the real permission check happens when the post is scraped |
| `posts[].timestamp` | `string` | Relative time string (e.g. "3mo", "2w", "1d") |
| `posts[].likes` | `number` |  |
| `posts[].comments` | `number` |  |
| `posts[].shares` | `number` |  |
| `posts[].author` | `object` |  |
| `posts[].author.name` | `string` |  |
| `posts[].author.profileUrl` | `string` |  |
| `posts[].author.profilePicture` | `string` |  |
| `posts[].author.type` | `list` |  |
| `posts[].authorHeadline` | `string` |  |
| `posts[].isEdited` | `boolean` |  |
| `posts[].isArticle` | `boolean` |  |
| `posts[].isRepost` | `boolean` |  |
| `pagination` | `object` |  |
| `pagination.start` | `number` |  |
| `pagination.count` | `number` | Posts actually returned |
| `pagination.requested` | `number` | Count originally asked for, before the cap |
| `pagination.capped` | `number` | Ceiling actually applied (30 max) |
| `pagination.total` | `number` | Always null — the underlying pager reports only whether another page exists, never a result total |
| `pagination.hasMore` | `boolean` |  |
| `pagination.nextStart` | `number` |  |
| `pagination.batchesFetched` | `number` |  |
| `pagination.fetchDurationMs` | `number` |  |
| `filters` | `object` |  |
| `filters.datePosted` | `string` |  |
| `filters.sortBy` | `string` |  |
| `filters.authorJobTitles` | `array` |  |
| `searchId` | `string` | Always null |
| `message` | `string` |  |
