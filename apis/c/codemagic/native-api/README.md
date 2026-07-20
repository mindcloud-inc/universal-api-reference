# Codemagic: Native API Reference

A consolidated summary of Codemagic's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://codemagic.io/api/v3/schema
- **OpenAPI specification:** https://codemagic.io/api/v3/schema/openapi.json
- **API base URL:** `https://codemagic.io`

## Authentication

### Codemagic API Token

Codemagic personal API token sent in the x-auth-token request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-auth-token: <apiKey>
```

[Official authentication documentation](https://codemagic.io/api/v3/schema)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `cursor`. The total page count is read from `total_pages`. The current page number is read from `current_page`.

## Pagination

Use `page_size` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Import Tester Group Contacts](actions/bulk-import-tester-group-contacts.md) | `POST /api/v3/tester-groups/:tester_group_id/contacts` | [docs](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdContactsBulkImport) |
| [Bulk Import Variables For Group](actions/bulk-import-variables-for-group.md) | `POST /api/v3/variable-groups/:variable_group_id/variables` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdVariablesBulkImport) |
| [Create App Tester Group](actions/create-app-tester-group.md) | `POST /api/v3/apps/:app_id/tester-groups` | [docs](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3AppsAppIdTesterGroupsCreateTesterGroup) |
| [Create App Variable Group](actions/create-app-variable-group.md) | `POST /api/v3/apps/:app_id/variable-groups` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3AppsAppIdVariableGroupsCreateVariableGroup) |
| [Create Team Variable Group](actions/create-team-variable-group.md) | `POST /api/v3/teams/:team_id/variable-groups` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3TeamsTeamIdVariableGroupsCreateVariableGroup) |
| [Delete Tester Group Contact](actions/delete-tester-group-contact.md) | `DELETE /api/v3/tester-groups/:tester_group_id/contacts/:contact_id` | [docs](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdContactsContactIdDeleteContact) |
| [Get App Preview](actions/get-app-preview.md) | `GET /api/v3/previews/:preview_id` | [docs](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3PreviewsPreviewIdGetPreviewInformation) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /api/v3/user` | [docs](https://codemagic.io/api/v3/schema#tag/Users/operation/ApiV3UserGetUser) |
| [Get Build](actions/get-build.md) | `GET /api/v3/builds/:build_id` | [docs](https://codemagic.io/api/v3/schema#tag/Builds/operation/ApiV3BuildsBuildIdGetBuild) |
| [Get Build Actions](actions/get-build-actions.md) | `GET /api/v3/builds/:build_id/actions` | [docs](https://codemagic.io/api/v3/schema#tag/Builds/operation/ApiV3BuildsBuildIdActionsGetBuildActions) |
| [Get Build Remote Access](actions/get-build-remote-access.md) | `GET /api/v3/builds/:build_id/remote-access` | [docs](https://codemagic.io/api/v3/schema#tag/Builds/operation/ApiV3BuildsBuildIdRemoteAccessGetBuildRemoteAccess) |
| [Get Meta Information](actions/get-meta-information.md) | `GET /api/v3/meta` | [docs](https://codemagic.io/api/v3/schema#tag/Meta/operation/ApiV3MetaGetMeta) |
| [Get OTA Account Info](actions/get-ota-account-info.md) | `GET /api/v3/over-the-air-updates` | [docs](https://codemagic.io/api/v3/schema#tag/Over-the-air%20Updates/operation/ApiV3OverTheAirUpdatesGetAccountInfo) |
| [Get OTA Team Usage](actions/get-ota-team-usage.md) | `GET /api/v3/over-the-air-updates/:team_id/usage` | [docs](https://codemagic.io/api/v3/schema#tag/Over-the-air%20Updates/operation/ApiV3OverTheAirUpdatesTeamIdUsageGetUsage) |
| [Get Shared App Preview](actions/get-shared-app-preview.md) | `GET /api/v3/shared-previews/:shared_preview_id` | [docs](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3SharedPreviewsSharedPreviewIdGetSharedPreview) |
| [Get Shorebird Metadata](actions/get-shorebird-metadata.md) | `GET /api/v3/meta/shorebird` | [docs](https://codemagic.io/api/v3/schema#tag/Meta/operation/ApiV3MetaShorebirdGetShorebirdMeta) |
| [Get Team](actions/get-team.md) | `GET /api/v3/teams/:team_id` | [docs](https://codemagic.io/api/v3/schema#tag/Teams/operation/ApiV3TeamsTeamIdGetTeam) |
| [Get Tester Group](actions/get-tester-group.md) | `GET /api/v3/tester-groups/:tester_group_id` | [docs](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdGetGroup) |
| [Get User Preferences](actions/get-user-preferences.md) | `GET /api/v3/user/preferences` | [docs](https://codemagic.io/api/v3/schema#tag/Users/operation/ApiV3UserPreferencesGetPreferences) |
| [Get Variable](actions/get-variable.md) | `GET /api/v3/variable-groups/:variable_group_id/variables/:variable_id` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdVariablesVariableIdGetVariable) |
| [Get Variable Group](actions/get-variable-group.md) | `GET /api/v3/variable-groups/:variable_group_id` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdGetGroup) |
| [List App Tester Groups](actions/list-app-tester-groups.md) | `GET /api/v3/apps/:app_id/tester-groups` | [docs](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3AppsAppIdTesterGroupsGetTesterGroups) |
| [List App Variable Groups](actions/list-app-variable-groups.md) | `GET /api/v3/apps/:app_id/variable-groups` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3AppsAppIdVariableGroupsGetVariableGroups) |
| [List Authenticated User Apps](actions/list-authenticated-user-apps.md) | `GET /api/v3/user/apps` | [docs](https://codemagic.io/api/v3/schema#tag/Applications/operation/ApiV3UserAppsGetApps) |
| [List Authenticated User Teams](actions/list-authenticated-user-teams.md) | `GET /api/v3/user/teams` | [docs](https://codemagic.io/api/v3/schema#tag/Teams/operation/ApiV3UserTeamsGetTeams) |
| [List OTA Projects](actions/list-ota-projects.md) | `GET /api/v3/over-the-air-updates/:team_id/projects` | [docs](https://codemagic.io/api/v3/schema#tag/Over-the-air%20Updates/operation/ApiV3OverTheAirUpdatesTeamIdProjectsListProjects) |
| [List Team App Previews](actions/list-team-app-previews.md) | `GET /api/v3/teams/:team_id/previews` | [docs](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3TeamsTeamIdPreviewsListTeamPreviews) |
| [List Team Apps](actions/list-team-apps.md) | `GET /api/v3/teams/:team_id/apps` | [docs](https://codemagic.io/api/v3/schema#tag/Applications/operation/ApiV3TeamsTeamIdAppsListTeamApps) |
| [List Team Builds](actions/list-team-builds.md) | `GET /api/v3/teams/:team_id/builds` | [docs](https://codemagic.io/api/v3/schema#tag/Builds/operation/ApiV3TeamsTeamIdBuildsListTeamBuilds) |
| [List Team Members](actions/list-team-members.md) | `GET /api/v3/teams/:team_id/members` | [docs](https://codemagic.io/api/v3/schema#tag/Team%20Members/operation/ApiV3TeamsTeamIdMembersListTeamMembers) |
| [List Team Variable Groups](actions/list-team-variable-groups.md) | `GET /api/v3/teams/:team_id/variable-groups` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3TeamsTeamIdVariableGroupsGetVariableGroups) |
| [List Tester Group Contacts](actions/list-tester-group-contacts.md) | `GET /api/v3/tester-groups/:tester_group_id/contacts` | [docs](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdContactsListContacts) |
| [List User Notifications](actions/list-user-notifications.md) | `GET /api/v3/user/notifications` | [docs](https://codemagic.io/api/v3/schema#tag/Users/operation/ApiV3UserNotificationsGetNotifications) |
| [List Variables For Group](actions/list-variables-for-group.md) | `GET /api/v3/variable-groups/:variable_group_id/variables` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdVariablesGetVariables) |
| [Share App Preview](actions/share-app-preview.md) | `POST /api/v3/previews/:preview_id/share` | [docs](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3PreviewsPreviewIdShareSharePreview) |
| [Start App Preview](actions/start-app-preview.md) | `POST /api/v3/builds/:build_id/preview` | [docs](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3BuildsBuildIdPreviewStartPreview) |
| [Stop App Preview](actions/stop-app-preview.md) | `DELETE /api/v3/previews/:preview_id` | [docs](https://codemagic.io/api/v3/schema#tag/App%20Previews/operation/ApiV3PreviewsPreviewIdStopPreview) |
| [Update Tester Group](actions/update-tester-group.md) | `PATCH /api/v3/tester-groups/:tester_group_id` | [docs](https://codemagic.io/api/v3/schema#tag/Tester%20Groups/operation/ApiV3TesterGroupsTesterGroupIdUpdateTesterGroup) |
| [Update Variable](actions/update-variable.md) | `PATCH /api/v3/variable-groups/:variable_group_id/variables/:variable_id` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdVariablesVariableIdUpdateVariable) |
| [Update Variable Group](actions/update-variable-group.md) | `PATCH /api/v3/variable-groups/:variable_group_id` | [docs](https://codemagic.io/api/v3/schema#tag/Secrets%20and%20Environment%20Vars/operation/ApiV3VariableGroupsVariableGroupIdUpdateGroup) |
