# Codeberg: Native API Reference

A consolidated summary of Codeberg's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://forgejo.org/docs/v13.0/user/api-usage/
- **OpenAPI specification:** https://codeberg.org/swagger.v1.json
- **API base URL:** `https://codeberg.org/api/v1`

## Authentication

### Personal Access Token

Authenticate with a Codeberg personal access token. Requests use the Forgejo Authorization header format: token <personal_access_token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.codeberg.org/advanced/access-token/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 30; accepted range 1–50). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check New Notifications](actions/check-new-notifications.md) | `GET /notifications/new` | [docs](https://codeberg.org/api/swagger#/notification/notifyNewAvailable) |
| [Get ActivityPub Instance Actor](actions/get-activitypub-instance-actor.md) | `GET /activitypub/actor` | [docs](https://codeberg.org/api/swagger#/activitypub/activitypubInstanceActor) |
| [Get API Settings](actions/get-api-settings.md) | `GET /settings/api` | [docs](https://codeberg.org/api/swagger#/settings/getGeneralAPISettings) |
| [Get Attachment Settings](actions/get-attachment-settings.md) | `GET /settings/attachment` | [docs](https://codeberg.org/api/swagger#/settings/getGeneralAttachmentSettings) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://codeberg.org/api/swagger#/user/userGetCurrent) |
| [Get Current User Quota](actions/get-current-user-quota.md) | `GET /user/quota` | [docs](https://codeberg.org/api/swagger#/user/userGetQuota) |
| [Get Current User Settings](actions/get-current-user-settings.md) | `GET /user/settings` | [docs](https://codeberg.org/api/swagger#/user/getUserSettings) |
| [Get Default GPG Signing Key](actions/get-default-gpg-signing-key.md) | `GET /signing-key.gpg` | [docs](https://codeberg.org/api/swagger#/miscellaneous/getSigningKey) |
| [Get Default SSH Signing Key](actions/get-default-ssh-signing-key.md) | `GET /signing-key.ssh` | [docs](https://codeberg.org/api/swagger#/miscellaneous/getSSHSigningKey) |
| [Get Forgejo Version](actions/get-forgejo-version.md) | `GET /version` | [docs](https://codeberg.org/api/swagger#/miscellaneous/getVersion) |
| [Get Node Info](actions/get-node-info.md) | `GET /nodeinfo` | [docs](https://codeberg.org/api/swagger#/miscellaneous/getNodeInfo) |
| [Get Repository Settings](actions/get-repository-settings.md) | `GET /settings/repository` | [docs](https://codeberg.org/api/swagger#/settings/getGeneralRepositorySettings) |
| [Get UI Settings](actions/get-ui-settings.md) | `GET /settings/ui` | [docs](https://codeberg.org/api/swagger#/settings/getGeneralUISettings) |
| [List Blocked Users](actions/list-blocked-users.md) | `GET /user/list_blocked` | [docs](https://codeberg.org/api/swagger#/user/userListBlockedUsers) |
| [List Current User Followers](actions/list-current-user-followers.md) | `GET /user/followers` | [docs](https://codeberg.org/api/swagger#/user/userCurrentListFollowers) |
| [List Current User Following](actions/list-current-user-following.md) | `GET /user/following` | [docs](https://codeberg.org/api/swagger#/user/userCurrentListFollowing) |
| [List Current User GPG Keys](actions/list-current-user-gpg-keys.md) | `GET /user/gpg_keys` | [docs](https://codeberg.org/api/swagger#/user/userCurrentListGPGKeys) |
| [List Current User Organizations](actions/list-current-user-organizations.md) | `GET /user/orgs` | [docs](https://codeberg.org/api/swagger#/organization/orgListCurrentUserOrgs) |
| [List Current User Public Keys](actions/list-current-user-public-keys.md) | `GET /user/keys` | [docs](https://codeberg.org/api/swagger#/user/userCurrentListKeys) |
| [List Current User Quota Artifacts](actions/list-current-user-quota-artifacts.md) | `GET /user/quota/artifacts` | [docs](https://codeberg.org/api/swagger#/user/userListQuotaArtifacts) |
| [List Current User Quota Attachments](actions/list-current-user-quota-attachments.md) | `GET /user/quota/attachments` | [docs](https://codeberg.org/api/swagger#/user/userListQuotaAttachments) |
| [List Current User Quota Packages](actions/list-current-user-quota-packages.md) | `GET /user/quota/packages` | [docs](https://codeberg.org/api/swagger#/user/userListQuotaPackages) |
| [List Current User Repositories](actions/list-current-user-repositories.md) | `GET /user/repos` | [docs](https://codeberg.org/api/swagger#/user/userCurrentListRepos) |
| [List Current User Webhooks](actions/list-current-user-webhooks.md) | `GET /user/hooks` | [docs](https://codeberg.org/api/swagger#/user/userListHooks) |
| [List Gitignore Templates](actions/list-gitignore-templates.md) | `GET /gitignore/templates` | [docs](https://codeberg.org/api/swagger#/miscellaneous/listGitignoresTemplates) |
| [List Label Templates](actions/list-label-templates.md) | `GET /label/templates` | [docs](https://codeberg.org/api/swagger#/miscellaneous/listLabelTemplates) |
| [List License Templates](actions/list-license-templates.md) | `GET /licenses` | [docs](https://codeberg.org/api/swagger#/miscellaneous/listLicenseTemplates) |
| [List Notifications](actions/list-notifications.md) | `GET /notifications` | [docs](https://codeberg.org/api/swagger#/notification/notifyGetList) |
| [List Organizations](actions/list-organizations.md) | `GET /orgs` | [docs](https://codeberg.org/api/swagger#/organization/orgGetAll) |
| [List Starred Repositories](actions/list-starred-repositories.md) | `GET /user/starred` | [docs](https://codeberg.org/api/swagger#/user/userCurrentListStarred) |
| [List Stopwatches](actions/list-stopwatches.md) | `GET /user/stopwatches` | [docs](https://codeberg.org/api/swagger#/user/userGetStopWatches) |
| [List User Actions Variables](actions/list-user-actions-variables.md) | `GET /user/actions/variables` | [docs](https://codeberg.org/api/swagger#/user/getUserVariablesList) |
| [List User Emails](actions/list-user-emails.md) | `GET /user/emails` | [docs](https://codeberg.org/api/swagger#/user/userListEmails) |
| [List User OAuth2 Applications](actions/list-user-oauth2-applications.md) | `GET /user/applications/oauth2` | [docs](https://codeberg.org/api/swagger#/user/userGetOAuth2Applications) |
| [List User Teams](actions/list-user-teams.md) | `GET /user/teams` | [docs](https://codeberg.org/api/swagger#/user/userListTeams) |
| [List User Tracked Times](actions/list-user-tracked-times.md) | `GET /user/times` | [docs](https://codeberg.org/api/swagger#/user/userCurrentTrackedTimes) |
| [List Watched Repositories](actions/list-watched-repositories.md) | `GET /user/subscriptions` | [docs](https://codeberg.org/api/swagger#/user/userCurrentListSubscriptions) |
| [Search Issues](actions/search-issues.md) | `GET /repos/issues/search` | [docs](https://codeberg.org/api/swagger#/issue/issueSearchIssues) |
| [Search Repositories](actions/search-repositories.md) | `GET /repos/search` | [docs](https://codeberg.org/api/swagger#/repository/repoSearch) |
| [Search Users](actions/search-users.md) | `GET /users/search` | [docs](https://codeberg.org/api/swagger#/user/userSearch) |
