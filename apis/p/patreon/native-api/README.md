# Patreon: Native API Reference

A consolidated summary of Patreon's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.patreon.com
- **API base URL:** `https://www.patreon.com/api/oauth2/v2`

## Authentication

### Patreon OAuth2

Connect Patreon with OAuth2 to access creator identity, campaigns, members, posts, and webhooks.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.patreon.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://www.patreon.com/api/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `identity identity[email] identity.memberships campaigns campaigns.members campaigns.members[email] campaigns.members.address campaigns.posts w:campaigns.webhook`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://www.patreon.com/api/oauth2/token.

[Official authentication documentation](https://docs.patreon.com/#oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud Patreon` |

The next-page cursor is read from `input.meta.pagination.cursors.next`.

## Pagination

Use `page[count]` in the query string to set the page size. Use `page[cursor]` in the query string as the pagination cursor.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.patreon.com#post-api-oauth2-v2-webhooks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://docs.patreon.com#delete-api-oauth2-v2-webhooks-id) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://docs.patreon.com#get-api-oauth2-v2-campaigns-campaign_id) |
| [Get Identity](actions/get-identity.md) | `GET /identity` | [docs](https://docs.patreon.com#get-api-oauth2-v2-identity) |
| [Get Member](actions/get-member.md) | `GET /members/:memberId` | [docs](https://docs.patreon.com#get-api-oauth2-v2-members-member_id) |
| [Get Post](actions/get-post.md) | `GET /posts/:postId` | [docs](https://docs.patreon.com#get-api-oauth2-v2-posts-id) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://docs.patreon.com#get-api-oauth2-v2-campaigns) |
| [List Members](actions/list-members.md) | `GET /campaigns/:campaignId/members` | [docs](https://docs.patreon.com#get-api-oauth2-v2-campaigns-campaign_id-members) |
| [List Posts](actions/list-posts.md) | `GET /campaigns/:campaignId/posts` | [docs](https://docs.patreon.com#get-api-oauth2-v2-campaigns-campaign_id-posts) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.patreon.com#get-api-oauth2-v2-webhooks) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:webhookId` | [docs](https://docs.patreon.com#patch-api-oauth2-v2-webhooks-id) |
