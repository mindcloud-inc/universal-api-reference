# Facebook: Native API Reference

A consolidated summary of Facebook's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.facebook.com/docs/
- **API base URL:** `https://graph.facebook.com/v25.0`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.facebook.com/v24.0/dialog/oauth to approve access.
2. Exchange the returned authorization code with a GET request to https://graph.facebook.com/v24.0/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `pages_read_user_content read_insights pages_read_engagement ads_read pages_show_list business_management pages_manage_posts publish_video instagram_basic instagram_content_publish`.

[Official authentication documentation](https://developers.facebook.com/documentation/facebook-login/guides/access-tokens)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The next-page cursor is read from `paging.next`.

## Pagination

Use `limit` in the query string to set the page size. Use `after` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ad Account Ads Query](actions/ad-account-ads-query.md) | `GET https://graph.facebook.com/v23.0/:adAccountID/ads` |  |
| [Ad Campaign Query](actions/ad-campaign-query.md) | `GET /:accountID` |  |
| [Create Instagram Carousel Container](actions/create-instagram-carousel-container.md) | `POST https://graph.facebook.com/v26.0/:instagramAccountId/media` | [docs](https://developers.facebook.com/documentation/instagram-platform/instagram-graph-api/reference/ig-user/media) |
| [Create Instagram Image Container](actions/create-instagram-image-container.md) | `POST https://graph.facebook.com/v26.0/:instagramAccountId/media` | [docs](https://developers.facebook.com/documentation/instagram-platform/instagram-graph-api/reference/ig-user/media) |
| [Create Instagram Image Story Container](actions/create-instagram-image-story-container.md) | `POST https://graph.facebook.com/v26.0/:instagramAccountId/media` | [docs](https://developers.facebook.com/documentation/instagram-platform/instagram-graph-api/reference/ig-user/media) |
| [Create Instagram Resumable Reel Container](actions/create-instagram-resumable-reel-container.md) | `POST https://graph.facebook.com/v26.0/:instagramAccountId/media` | [docs](https://developers.facebook.com/documentation/instagram-platform/instagram-graph-api/reference/ig-user/media) |
| [Create Page Photo](actions/create-page-photo.md) | `POST /:pageId/photos` | [docs](https://developers.facebook.com/docs/graph-api/reference/page/photos/) |
| [Create Page Post](actions/create-page-post.md) | `POST /:pageId/feed` | [docs](https://developers.facebook.com/docs/graph-api/reference/page/feed/) |
| [Create Page Video](actions/create-page-video.md) | `POST /:pageId/videos` | [docs](https://developers.facebook.com/docs/graph-api/reference/page/videos/) |
| [Get Instagram Container Status](actions/get-instagram-container-status.md) | `GET https://graph.facebook.com/v26.0/:containerId` | [docs](https://developers.facebook.com/documentation/instagram-platform/instagram-graph-api/reference/ig-container) |
| [Get Instagram Publishing Limit](actions/get-instagram-publishing-limit.md) | `GET https://graph.facebook.com/v26.0/:instagramAccountId/content_publishing_limit` | [docs](https://developers.facebook.com/documentation/instagram-platform/instagram-graph-api/reference/ig-user/content_publishing_limit) |
| [Get Owned Pages](actions/get-owned-pages.md) | `GET :businessId/owned_pages?fields=id,name,access_token` |  |
| [Get Page](actions/get-page.md) | `GET :pageId` | [docs](https://developers.facebook.com/docs/graph-api/reference/page/) |
| [Get Page Insights](actions/get-page-insights.md) | `GET /:pageId/insights` | [docs](https://developers.facebook.com/docs/graph-api/reference/v25.0/insights) |
| [List Ad Accounts](actions/list-ad-accounts.md) | `GET me/adaccounts` | [docs](https://developers.facebook.com/docs/graph-api/reference/user/adaccounts/) |
| [List Businesses](actions/list-businesses.md) | `GET /me/businesses` | [docs](https://developers.facebook.com/docs/graph-api/reference/user/businesses/) |
| [List Daily Ad Insights](actions/list-daily-ad-insights.md) | `GET :adAccountId/insights` | [docs](https://developers.facebook.com/docs/graph-api/reference/adaccount/insights/) |
| [List Pages](actions/list-pages.md) | `GET me/accounts` | [docs](https://developers.facebook.com/docs/graph-api/reference/user/accounts/) |
| [Publish Instagram Media](actions/publish-instagram-media.md) | `POST https://graph.facebook.com/v26.0/:instagramAccountId/media_publish` | [docs](https://developers.facebook.com/documentation/instagram-platform/instagram-graph-api/reference/ig-user/media_publish) |
| [Upload Instagram Container Video](actions/upload-instagram-container-video.md) | `POST https://rupload.facebook.com/ig-api-upload/v26.0/:containerId` | [docs](https://developers.facebook.com/documentation/instagram-platform/instagram-graph-api/reference/ig-user/media) |
