# Google Groups: Native API Reference

A consolidated summary of Google Groups's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/admin/directory/v1/guides/manage-groups
- **API base URL:** `https://groups.google.com`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/admin.directory.group https://www.googleapis.com/auth/apps.groups.settings`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/identity/protocols/oauth2/web-server)

## API conventions

Responses from this API use JSON. Response data is read from `groups`. The next-page cursor is read from `nextPageToken`.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Group Member](actions/add-group-member.md) | `POST https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/insert) |
| [Check Group Membership](actions/check-group-membership.md) | `GET https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/hasMember/:memberKey` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/hasMember) |
| [Create Group](actions/create-group.md) | `POST https://admin.googleapis.com/admin/directory/v1/groups` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/insert) |
| [Create Group Alias](actions/create-group-alias.md) | `POST https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/aliases` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups.aliases/insert) |
| [Delete Group](actions/delete-group.md) | `DELETE https://admin.googleapis.com/admin/directory/v1/groups/:groupKey` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/delete) |
| [Delete Group Alias](actions/delete-group-alias.md) | `DELETE https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/aliases/:alias` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups.aliases/delete) |
| [Delete Group Member](actions/delete-group-member.md) | `DELETE https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members/:memberKey` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/delete) |
| [Get Group](actions/get-group.md) | `GET https://admin.googleapis.com/admin/directory/v1/groups/:groupKey` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/get) |
| [Get Group Member](actions/get-group-member.md) | `GET https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members/:memberKey` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/get) |
| [Get Group Settings](actions/get-group-settings.md) | `GET https://www.googleapis.com/groups/v1/groups/:groupUniqueId` | [docs](https://developers.google.com/workspace/admin/groups-settings/v1/reference/groups/get) |
| [List Group Aliases](actions/list-group-aliases.md) | `GET https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/aliases` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups.aliases/list) |
| [List Group Members](actions/list-group-members.md) | `GET https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/list) |
| [List Groups](actions/list-groups.md) | `GET https://admin.googleapis.com/admin/directory/v1/groups` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/list) |
| [Patch Group](actions/patch-group.md) | `PATCH https://admin.googleapis.com/admin/directory/v1/groups/:groupKey` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/patch) |
| [Patch Group Member](actions/patch-group-member.md) | `PATCH https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members/:memberKey` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/patch) |
| [Patch Group Settings](actions/patch-group-settings.md) | `PATCH https://www.googleapis.com/groups/v1/groups/:groupUniqueId` | [docs](https://developers.google.com/workspace/admin/groups-settings/v1/reference/groups/patch) |
| [Update Group](actions/update-group.md) | `PUT https://admin.googleapis.com/admin/directory/v1/groups/:groupKey` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/update) |
| [Update Group Member](actions/update-group-member.md) | `PUT https://admin.googleapis.com/admin/directory/v1/groups/:groupKey/members/:memberKey` | [docs](https://developers.google.com/admin-sdk/directory/reference/rest/v1/members/update) |
| [Update Group Settings](actions/update-group-settings.md) | `PUT https://www.googleapis.com/groups/v1/groups/:groupUniqueId` | [docs](https://developers.google.com/workspace/admin/groups-settings/v1/reference/groups/update) |
