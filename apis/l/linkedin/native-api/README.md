# LinkedIn: Native API Reference

A consolidated summary of LinkedIn's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/linkedin/
- **API base URL:** `https://api.linkedin.com`

## Authentication

### OAuth2

LinkedIn OAuth 2.0 / OpenID Connect

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.linkedin.com/oauth/v2/authorization to approve access.
2. Exchange the returned authorization code with a POST request to https://www.linkedin.com/oauth/v2/accessToken.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid profile email w_member_social`.

[Official authentication documentation](https://learn.microsoft.com/en-us/linkedin/shared/authentication/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `LinkedIn-Version` | `202511` |
| `X-Restli-Protocol-Version` | `2.0.0` |

## Pagination

Use `count` in the query string to set the page size. Use `start` in the query string as the record offset.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | `POST /rest/posts` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/posts-api?view=li-lms-2025-11) |
| [Delete Post](actions/delete-post.md) | `DELETE /rest/posts/:encodedPostUrn` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/posts-api?view=li-lms-2025-11) |
| [Get Document](actions/get-document.md) | `GET /rest/documents/:documentUrn` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/documents-api?view=li-lms-2026-02) |
| [Get Image](actions/get-image.md) | `GET /rest/images/:imageUrn` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/images-api?view=li-lms-2026-01) |
| [Get User Info](actions/get-user-info.md) | `GET /v2/userinfo` | [docs](https://learn.microsoft.com/en-us/linkedin/consumer/integrations/self-serve/sign-in-with-linkedin) |
| [Get Video](actions/get-video.md) | `GET /rest/videos/:videoUrn` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/videos-api?view=li-lms-2026-02) |
| [Initialize Document Upload](actions/initialize-document-upload.md) | `POST /rest/documents?action=initializeUpload` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/documents-api?view=li-lms-2026-02) |
| [Initialize Image Upload](actions/initialize-image-upload.md) | `POST /rest/images?action=initializeUpload` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/images-api?view=li-lms-2026-01) |
| [Initialize Video Upload](actions/initialize-video-upload.md) | `POST /rest/videos?action=initializeUpload` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/videos-api?view=li-lms-2026-02) |
| [Update Post](actions/update-post.md) | `POST /rest/posts/:encodedPostUrn` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/community-management/shares/posts-api?view=li-lms-2025-11) |
