# Qntrl: Native API Reference

A consolidated summary of Qntrl's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://core.qntrl.com/apidoc.html
- **API base URL:** `https://coreapi.qntrl.com/blueprint/api`

## Authentication

### OAuth 2.0

Connect Qntrl with Zoho OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.zoho.com/oauth/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.zoho.com/oauth/v2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `Qntrl.org.READ Qntrl.job.READ Qntrl.attachment.READ Qntrl.jobcomment.READ Qntrl.transition.READ Qntrl.layout.READ Qntrl.customfield.READ Qntrl.blueprint.READ Qntrl.stage.READ Qntrl.user.READ Qntrl.customview.READ Qntrl.userprofile.READ Qntrl.role.READ Qntrl.reports.READ Orchestly.table.READ`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.zoho.com/oauth/v2/token.

[Official authentication documentation](https://core.qntrl.com/apidoc.html)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Export Users](actions/export-users.md) | `GET /[:org_id]/user/export` | [docs](https://core.qntrl.com/apidoc.html#Download) |
| [Get Attachment Details](actions/get-attachment-details.md) | `GET /[:org_id]/job/[:job_id]/attachment/[:attachment_id]` | [docs](https://core.qntrl.com/apidoc.html) |
| [Get Blueprint Details](actions/get-blueprint-details.md) | `GET /[:org_id]/blueprint/[:blueprint_id]` | [docs](https://core.qntrl.com/apidoc.html#ProcessDetails) |
| [Get Card Comment Details](actions/get-card-comment-details.md) | `GET /[:org_id]/job/[:job_id]/comment/[:comment_id]` | [docs](https://core.qntrl.com/apidoc.html#GetComment) |
| [Get Card Details](actions/get-card-details.md) | `GET /[:org_id]/job/[:job_id]` | [docs](https://core.qntrl.com/apidoc.html#GetJob) |
| [Get Custom Field Details](actions/get-custom-field-details.md) | `GET /[:org_id]/customfield/[:customfield_id]` | [docs](https://core.qntrl.com/apidoc.html#CustomFieldsDetails) |
| [Get Custom View Details](actions/get-custom-view-details.md) | `GET /[:org_id]/customview/[:customview_id]` | [docs](https://core.qntrl.com/apidoc.html) |
| [Get Form Details](actions/get-form-details.md) | `GET /[:org_id]/layout/[:layout_id]` | [docs](https://core.qntrl.com/apidoc.html#getServiceDetails) |
| [Get My User Details](actions/get-my-user-details.md) | `GET /user/myinfo` | [docs](https://core.qntrl.com/apidoc.html#myinfo) |
| [Get Organization Details](actions/get-organization-details.md) | `GET /org/[:org_id]` | [docs](https://core.qntrl.com/apidoc.html#GetOrgDetails) |
| [Get Profile Details](actions/get-profile-details.md) | `GET /[:org_id]/profile/[:profile_id]` | [docs](https://core.qntrl.com/apidoc.html#GetProfileDetails) |
| [Get Report Details](actions/get-report-details.md) | `GET /[:org_id]/reports/[:report_id]` | [docs](https://core.qntrl.com/apidoc.html#GetReport) |
| [Get Report Folder Details](actions/get-report-folder-details.md) | `GET /[:org_id]/reportfolder/[:reportfolder_id]` | [docs](https://core.qntrl.com/apidoc.html#GetFolder) |
| [Get Role Details](actions/get-role-details.md) | `GET /[:org_id]/role/[:role_id]` | [docs](https://core.qntrl.com/apidoc.html#getRole) |
| [Get Row Details](actions/get-row-details.md) | `GET /[:org_id]/table/[:table_id]/row/[:row_id]` | [docs](https://core.qntrl.com/apidoc.html#getRow) |
| [Get Stage Details](actions/get-stage-details.md) | `GET /[:org_id]/stage/[:stage_id]` | [docs](https://core.qntrl.com/apidoc.html#GetStage) |
| [Get Table Details](actions/get-table-details.md) | `GET /[:org_id]/table/[:table_id]` | [docs](https://core.qntrl.com/apidoc.html#GetTable) |
| [Get Transition Rule](actions/get-transition-rule.md) | `GET /[:org_id]/transitionrule/[:transition_rule_id]` | [docs](https://core.qntrl.com/apidoc.html#getTransitionRule) |
| [Get User Activity](actions/get-user-activity.md) | `GET /[:org_id]/user/activity/[:user_id]` | [docs](https://core.qntrl.com/apidoc.html#useractivity) |
| [Get User Details](actions/get-user-details.md) | `GET /[:org_id]/user/[:user_id]` | [docs](https://core.qntrl.com/apidoc.html#getuserdetails) |
| [List Active Blueprints](actions/list-active-blueprints.md) | `GET /[:org_id]/blueprint/active` | [docs](https://core.qntrl.com/apidoc.html#getActiveBlueprints) |
| [List Blueprints](actions/list-blueprints.md) | `GET /[:org_id]/blueprint` | [docs](https://core.qntrl.com/apidoc.html#GetAllBlueprints) |
| [List Card Activities](actions/list-card-activities.md) | `GET /[:org_id]/job/[:job_id]/activities` | [docs](https://core.qntrl.com/apidoc.html#Activities) |
| [List Card Attachments](actions/list-card-attachments.md) | `GET /[:org_id]/job/[:job_id]/attachment` | [docs](https://core.qntrl.com/apidoc.html#GetAttachments) |
| [List Card Comments](actions/list-card-comments.md) | `GET /[:org_id]/job/[:job_id]/comment` | [docs](https://core.qntrl.com/apidoc.html#GetAllComments) |
| [List Cards](actions/list-cards.md) | `GET /[:org_id]/job` | [docs](https://core.qntrl.com/apidoc.html#getAllJobs) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /[:org_id]/customfield` | [docs](https://core.qntrl.com/apidoc.html#GetAllCustomFields) |
| [List Custom Views](actions/list-custom-views.md) | `GET /[:org_id]/customview` | [docs](https://core.qntrl.com/apidoc.html#GetAllCustomViews) |
| [List Deleted Cards](actions/list-deleted-cards.md) | `GET /[:org_id]/job/deletedjobs` | [docs](https://core.qntrl.com/apidoc.html#getDeletedJobs) |
| [List Forms](actions/list-forms.md) | `GET /[:org_id]/layout` | [docs](https://core.qntrl.com/apidoc.html#getServices) |
| [List Next Card Transitions](actions/list-next-card-transitions.md) | `GET /[:org_id]/job/nexttransitions/[:job_id]` | [docs](https://core.qntrl.com/apidoc.html#GetNextTransitions) |
| [List Organizations](actions/list-organizations.md) | `GET /org` | [docs](https://core.qntrl.com/apidoc.html#GetAllOrgDetails) |
| [List Profile Permissions](actions/list-profile-permissions.md) | `GET /[:org_id]/profile/permissions/[:profile_id]` | [docs](https://core.qntrl.com/apidoc.html#getProfilePermissions) |
| [List Profiles](actions/list-profiles.md) | `GET /[:org_id]/profile` | [docs](https://core.qntrl.com/apidoc.html#GetAllProfiles) |
| [List Report Folders](actions/list-report-folders.md) | `GET /[:org_id]/reportfolder` | [docs](https://core.qntrl.com/apidoc.html#GetAllFolders) |
| [List Reports](actions/list-reports.md) | `GET /[:org_id]/reports` | [docs](https://core.qntrl.com/apidoc.html#GetAllCustomReports) |
| [List Roles](actions/list-roles.md) | `GET /[:org_id]/role` | [docs](https://core.qntrl.com/apidoc.html#getRoles) |
| [List Rows](actions/list-rows.md) | `GET /[:org_id]/table/[:table_id]/row` | [docs](https://core.qntrl.com/apidoc.html#getRows) |
| [List Stages](actions/list-stages.md) | `GET /[:org_id]/stage` | [docs](https://core.qntrl.com/apidoc.html#GetAllStages) |
| [List Tables](actions/list-tables.md) | `GET /[:org_id]/table` | [docs](https://core.qntrl.com/apidoc.html#GetAllTables) |
| [List User Dropdown Values](actions/list-user-dropdown-values.md) | `GET /[:org_id]/user/userpickvalues` | [docs](https://core.qntrl.com/apidoc.html#userpickvalues) |
| [List Users](actions/list-users.md) | `GET /[:org_id]/user` | [docs](https://core.qntrl.com/apidoc.html#getusers) |
