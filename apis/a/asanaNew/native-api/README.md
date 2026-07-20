# Asana: Native API Reference

A consolidated summary of Asana's API configuration and 168 documented operations, with links to official documentation.

- **Official docs:** https://developers.asana.com/reference/rest-api-reference
- **OpenAPI specification:** https://raw.githubusercontent.com/Asana/openapi/master/defs/asana_oas.yaml
- **API base URL:** `https://app.asana.com/api/1.0`

## Authentication

### OAuth 2.0

OAuth 2.0 for Asana API access with apps@mindcloud.co trial account.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.asana.com/-/oauth_authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://app.asana.com/-/oauth_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `default`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://app.asana.com/-/oauth_token.

[Official authentication documentation](https://developers.asana.com/docs/oauth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `next_page.offset`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (168 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add a collaborator to a goal](actions/add-a-collaborator-to-a-goal.md) | `POST goals/:goal_gid/addFollowers` | [docs](https://developers.asana.com/reference/addfollowers) |
| [Add a custom field to a portfolio](actions/add-a-custom-field-to-a-portfolio.md) | `POST portfolios/:portfolio_gid/addCustomFieldSetting` | [docs](https://developers.asana.com/reference/addcustomfieldsettingforportfolio) |
| [Add a custom field to a project](actions/add-a-custom-field-to-a-project.md) | `POST projects/:project_gid/addCustomFieldSetting` | [docs](https://developers.asana.com/reference/addcustomfieldsettingforproject) |
| [Add a portfolio item](actions/add-a-portfolio-item.md) | `POST portfolios/:portfolio_gid/addItem` | [docs](https://developers.asana.com/reference/additemforportfolio) |
| [Add a project to a task](actions/add-a-project-to-a-task.md) | `POST tasks/:task_gid/addProject` | [docs](https://developers.asana.com/reference/addprojectfortask) |
| [Add a supporting goal relationship](actions/add-a-supporting-goal-relationship.md) | `POST goals/:goal_gid/addSupportingRelationship` | [docs](https://developers.asana.com/reference/addsupportingrelationship) |
| [Add a tag to a task](actions/add-a-tag-to-a-task.md) | `POST tasks/:task_gid/addTag` | [docs](https://developers.asana.com/reference/addtagfortask) |
| [Add a user to a team](actions/add-a-user-to-a-team.md) | `POST teams/:team_gid/addUser` | [docs](https://developers.asana.com/reference/adduserforteam) |
| [Add a user to a workspace or organization](actions/add-a-user-to-a-workspace-or-organization.md) | `POST workspaces/:workspace_gid/addUser` | [docs](https://developers.asana.com/reference/adduserforworkspace) |
| [Add followers to a project](actions/add-followers-to-a-project.md) | `POST projects/:project_gid/addFollowers` | [docs](https://developers.asana.com/reference/addfollowersforproject) |
| [Add followers to a task](actions/add-followers-to-a-task.md) | `POST tasks/:task_gid/addFollowers` | [docs](https://developers.asana.com/reference/addfollowersfortask) |
| [Add task to section](actions/add-task-to-section.md) | `POST sections/:section_gid/addTask` | [docs](https://developers.asana.com/reference/addtaskforsection) |
| [Add users to a portfolio](actions/add-users-to-a-portfolio.md) | `POST portfolios/:portfolio_gid/addMembers` | [docs](https://developers.asana.com/reference/addmembersforportfolio) |
| [Add users to a project](actions/add-users-to-a-project.md) | `POST projects/:project_gid/addMembers` | [docs](https://developers.asana.com/reference/addmembersforproject) |
| [Create a custom field](actions/create-a-custom-field.md) | `POST custom_fields` | [docs](https://developers.asana.com/reference/createcustomfield) |
| [Create a goal](actions/create-a-goal.md) | `POST goals` | [docs](https://developers.asana.com/reference/creategoal) |
| [Create a goal metric](actions/create-a-goal-metric.md) | `POST goals/:goal_gid/setMetric` | [docs](https://developers.asana.com/reference/creategoalmetric) |
| [Create a membership](actions/create-a-membership.md) | `POST memberships` | [docs](https://developers.asana.com/reference/createprojectforteam) |
| [Create a portfolio](actions/create-a-portfolio.md) | `POST portfolios` | [docs](https://developers.asana.com/reference/createportfolio) |
| [Create a project](actions/create-a-project.md) | `POST projects` | [docs](https://developers.asana.com/reference/createproject) |
| [Create a project brief](actions/create-a-project-brief.md) | `POST projects/:project_gid/project_briefs` | [docs](https://developers.asana.com/reference/createprojectbrief) |
| [Create a project in a team](actions/create-a-project-in-a-team.md) | `POST teams/:team_gid/projects` | [docs](https://developers.asana.com/reference/createprojectforteam) |
| [Create a project in a workspace](actions/create-a-project-in-a-workspace.md) | `POST workspaces/:workspace_gid/projects` | [docs](https://developers.asana.com/reference/createprojectforworkspace) |
| [Create a project status](actions/create-a-project-status.md) | `POST projects/:project_gid/project_statuses` | [docs](https://developers.asana.com/reference/createprojectstatusforproject) |
| [Create a project template from a project](actions/create-a-project-template-from-a-project.md) | `POST projects/:project_gid/saveAsTemplate` | [docs](https://developers.asana.com/reference/projectsaveastemplate) |
| [Create a section in a project](actions/create-a-section-in-a-project.md) | `POST projects/:project_gid/sections` | [docs](https://developers.asana.com/reference/createsectionforproject) |
| [Create a status update](actions/create-a-status-update.md) | `POST status_updates` | [docs](https://developers.asana.com/reference/createstatusforobject) |
| [Create a story on a task](actions/create-a-story-on-a-task.md) | `POST tasks/:task_gid/stories` | [docs](https://developers.asana.com/reference/createstoryfortask) |
| [Create a subtask](actions/create-a-subtask.md) | `POST tasks/:task_gid/subtasks` | [docs](https://developers.asana.com/reference/createsubtaskfortask) |
| [Create a tag](actions/create-a-tag.md) | `POST tags` | [docs](https://developers.asana.com/reference/createtag) |
| [Create a tag in a workspace](actions/create-a-tag-in-a-workspace.md) | `POST workspaces/:workspace_gid/tags` | [docs](https://developers.asana.com/reference/createtagforworkspace) |
| [Create a task](actions/create-a-task.md) | `POST tasks` | [docs](https://developers.asana.com/reference/createtask) |
| [Create a team](actions/create-a-team.md) | `POST teams` | [docs](https://developers.asana.com/reference/createteam) |
| [Create an enum option](actions/create-an-enum-option.md) | `POST custom_fields/:custom_field_gid/enum_options` | [docs](https://developers.asana.com/reference/createenumoptionforcustomfield) |
| [Create an organization export request](actions/create-an-organization-export-request.md) | `POST organization_exports` | [docs](https://developers.asana.com/reference/createorganizationexport) |
| [Delete a custom field](actions/delete-a-custom-field.md) | `DELETE custom_fields/:custom_field_gid` | [docs](https://developers.asana.com/reference/deletecustomfield) |
| [Delete a goal](actions/delete-a-goal.md) | `DELETE goals/:goal_gid` | [docs](https://developers.asana.com/reference/deletegoal) |
| [Delete a portfolio](actions/delete-a-portfolio.md) | `DELETE portfolios/:portfolio_gid` | [docs](https://developers.asana.com/reference/deleteportfolio) |
| [Delete a project](actions/delete-a-project.md) | `DELETE projects/:project_gid` | [docs](https://developers.asana.com/reference/deleteproject) |
| [Delete a project brief](actions/delete-a-project-brief.md) | `DELETE project_briefs/:project_brief_gid` | [docs](https://developers.asana.com/reference/deleteprojectbrief) |
| [Delete a project status](actions/delete-a-project-status.md) | `DELETE project_statuses/:project_status_gid` | [docs](https://developers.asana.com/reference/deleteprojectstatus) |
| [Delete a section](actions/delete-a-section.md) | `DELETE sections/:section_gid` | [docs](https://developers.asana.com/reference/deletesection) |
| [Delete a status update](actions/delete-a-status-update.md) | `DELETE status_updates/:status_update_gid` | [docs](https://developers.asana.com/reference/deletestatus) |
| [Delete a story](actions/delete-a-story.md) | `DELETE stories/:story_gid` | [docs](https://developers.asana.com/reference/deletestory) |
| [Delete a tag](actions/delete-a-tag.md) | `DELETE tags/:tag_gid` | [docs](https://developers.asana.com/reference/deletetag) |
| [Delete a task](actions/delete-a-task.md) | `DELETE tasks/:task_gid` | [docs](https://developers.asana.com/reference/deletetask) |
| [Delete a webhook](actions/delete-a-webhook.md) | `DELETE webhooks/:webhook_gid` | [docs](https://developers.asana.com/reference/deletewebhook) |
| [Delete an attachment](actions/delete-an-attachment.md) | `DELETE attachments/:attachment_gid` | [docs](https://developers.asana.com/reference/deleteattachment) |
| [Duplicate a project](actions/duplicate-a-project.md) | `POST projects/:project_gid/duplicate` | [docs](https://developers.asana.com/reference/duplicateproject) |
| [Duplicate a task](actions/duplicate-a-task.md) | `POST tasks/:task_gid/duplicate` | [docs](https://developers.asana.com/reference/duplicatetask) |
| [Establish a webhook](actions/establish-a-webhook.md) | `POST webhooks` | [docs](https://developers.asana.com/reference/createwebhook) |
| [Get a custom field](actions/get-a-custom-field.md) | `GET custom_fields/:custom_field_gid` | [docs](https://developers.asana.com/reference/getcustomfield) |
| [Get a goal](actions/get-a-goal.md) | `GET goals/:goal_gid` | [docs](https://developers.asana.com/reference/getgoal) |
| [Get a goal relationship](actions/get-a-goal-relationship.md) | `GET goal_relationships/:goal_relationship_gid` | [docs](https://developers.asana.com/reference/getgoalrelationship) |
| [Get a job by id](actions/get-a-job-by-id.md) | `GET jobs/:job_gid` | [docs](https://developers.asana.com/reference/getjob) |
| [Get a portfolio](actions/get-a-portfolio.md) | `GET portfolios/:portfolio_gid` | [docs](https://developers.asana.com/reference/getportfolio) |
| [Get a portfolio membership](actions/get-a-portfolio-membership.md) | `GET portfolio_memberships/:portfolio_membership_gid` | [docs](https://developers.asana.com/reference/getportfoliomembership) |
| [Get a portfolio's custom fields](actions/get-a-portfolios-custom-fields.md) | `GET portfolios/:portfolio_gid/custom_field_settings` | [docs](https://developers.asana.com/reference/getcustomfieldsettingsforportfolio) |
| [Get a project](actions/get-a-project.md) | `GET projects/:project_gid` | [docs](https://developers.asana.com/reference/getproject) |
| [Get a project brief](actions/get-a-project-brief.md) | `GET project_briefs/:project_brief_gid` | [docs](https://developers.asana.com/reference/getprojectbrief) |
| [Get a project membership](actions/get-a-project-membership.md) | `GET project_memberships/:project_membership_gid` | [docs](https://developers.asana.com/reference/getprojectmembership) |
| [Get a project status](actions/get-a-project-status.md) | `GET project_statuses/:project_status_gid` | [docs](https://developers.asana.com/reference/getprojectstatus) |
| [Get a project template](actions/get-a-project-template.md) | `GET project_templates/:project_template_gid` | [docs](https://developers.asana.com/reference/getprojecttemplate) |
| [Get a project's custom fields](actions/get-a-projects-custom-fields.md) | `GET projects/:project_gid/custom_field_settings` | [docs](https://developers.asana.com/reference/getcustomfieldsettingsforproject) |
| [Get a section](actions/get-a-section.md) | `GET sections/:section_gid` | [docs](https://developers.asana.com/reference/getsection) |
| [Get a status update](actions/get-a-status-update.md) | `GET status_updates/:status_update_gid` | [docs](https://developers.asana.com/reference/getstatus) |
| [Get a story](actions/get-a-story.md) | `GET stories/:story_gid` | [docs](https://developers.asana.com/reference/getstory) |
| [Get a tag](actions/get-a-tag.md) | `GET tags/:tag_gid` | [docs](https://developers.asana.com/reference/gettag) |
| [Get a task](actions/get-a-task.md) | `GET tasks/:task_gid` | [docs](https://developers.asana.com/reference/gettask) |
| [Get a task's tags](actions/get-a-tasks-tags.md) | `GET tasks/:task_gid/tags` | [docs](https://developers.asana.com/reference/gettagsfortask) |
| [Get a team](actions/get-a-team.md) | `GET teams/:team_gid` | [docs](https://developers.asana.com/reference/getteam) |
| [Get a team membership](actions/get-a-team-membership.md) | `GET team_memberships/:team_membership_gid` | [docs](https://developers.asana.com/reference/getteammembership) |
| [Get a team's project templates](actions/get-a-teams-project-templates.md) | `GET teams/:team_gid/project_templates` | [docs](https://developers.asana.com/reference/getprojecttemplatesforteam) |
| [Get a team's projects](actions/get-a-teams-projects.md) | `GET teams/:team_gid/projects` | [docs](https://developers.asana.com/reference/getprojectsforteam) |
| [Get a time period](actions/get-a-time-period.md) | `GET time_periods/:time_period_gid` | [docs](https://developers.asana.com/reference/gettimeperiod) |
| [Get a user](actions/get-a-user.md) | `GET users/:user_gid` | [docs](https://developers.asana.com/reference/getuser) |
| [Get a user task list](actions/get-a-user-task-list.md) | `GET user_task_lists/:user_task_list_gid` | [docs](https://developers.asana.com/reference/getusertasklist) |
| [Get a user's favorites](actions/get-a-users-favorites.md) | `GET users/:user_gid/favorites` | [docs](https://developers.asana.com/reference/getfavoritesforuser) |
| [Get a user's task list](actions/get-a-users-task-list.md) | `GET users/:user_gid/user_task_list` | [docs](https://developers.asana.com/reference/getusertasklistforuser) |
| [Get a webhook](actions/get-a-webhook.md) | `GET webhooks/:webhook_gid` | [docs](https://developers.asana.com/reference/getwebhook) |
| [Get a workspace](actions/get-a-workspace.md) | `GET workspaces/:workspace_gid` | [docs](https://developers.asana.com/reference/getworkspace) |
| [Get a workspace membership](actions/get-a-workspace-membership.md) | `GET workspace_memberships/:workspace_membership_gid` | [docs](https://developers.asana.com/reference/getworkspacemembership) |
| [Get a workspace's custom fields](actions/get-a-workspaces-custom-fields.md) | `GET workspaces/:workspace_gid/custom_fields` | [docs](https://developers.asana.com/reference/getcustomfieldsforworkspace) |
| [Get all projects in a workspace](actions/get-all-projects-in-a-workspace.md) | `GET workspaces/:workspace_gid/projects` | [docs](https://developers.asana.com/reference/getprojectsforworkspace) |
| [Get an attachment](actions/get-an-attachment.md) | `GET attachments/:attachment_gid` | [docs](https://developers.asana.com/reference/getattachment) |
| [Get attachments from an object](actions/get-attachments-from-an-object.md) | `GET attachments` | [docs](https://developers.asana.com/reference/getattachmentsforobject) |
| [Get audit log events](actions/get-audit-log-events.md) | `GET workspaces/:workspace_gid/audit_log_events` | [docs](https://developers.asana.com/reference/getauditlogevents) |
| [Get dependencies from a task](actions/get-dependencies-from-a-task.md) | `GET tasks/:task_gid/dependencies` | [docs](https://developers.asana.com/reference/getdependenciesfortask) |
| [Get dependents from a task](actions/get-dependents-from-a-task.md) | `GET tasks/:task_gid/dependents` | [docs](https://developers.asana.com/reference/getdependentsfortask) |
| [Get details on an org export request](actions/get-details-on-an-org-export-request.md) | `GET organization_exports/:organization_export_gid` | [docs](https://developers.asana.com/reference/getorganizationexport) |
| [Get events on a resource](actions/get-events-on-a-resource.md) | `GET events` | [docs](https://developers.asana.com/reference/getevents) |
| [Get goal relationships](actions/get-goal-relationships.md) | `GET goal_relationships` | [docs](https://developers.asana.com/reference/getgoalrelationships) |
| [Get goals](actions/get-goals.md) | `GET goals` | [docs](https://developers.asana.com/reference/getgoals) |
| [Get memberships from a portfolio](actions/get-memberships-from-a-portfolio.md) | `GET portfolios/:portfolio_gid/portfolio_memberships` | [docs](https://developers.asana.com/reference/getportfoliomembershipsforportfolio) |
| [Get memberships from a project](actions/get-memberships-from-a-project.md) | `GET projects/:project_gid/project_memberships` | [docs](https://developers.asana.com/reference/getprojectmembershipsforproject) |
| [Get memberships from a team](actions/get-memberships-from-a-team.md) | `GET teams/:team_gid/team_memberships` | [docs](https://developers.asana.com/reference/getteammembershipsforteam) |
| [Get memberships from a user](actions/get-memberships-from-a-user.md) | `GET users/:user_gid/team_memberships` | [docs](https://developers.asana.com/reference/getteammembershipsforuser) |
| [Get multiple portfolio memberships](actions/get-multiple-portfolio-memberships.md) | `GET portfolio_memberships` | [docs](https://developers.asana.com/reference/getportfoliomemberships) |
| [Get multiple portfolios](actions/get-multiple-portfolios.md) | `GET portfolios` | [docs](https://developers.asana.com/reference/getportfolios) |
| [Get multiple project templates](actions/get-multiple-project-templates.md) | `GET project_templates` | [docs](https://developers.asana.com/reference/getprojecttemplates) |
| [Get multiple projects](actions/get-multiple-projects.md) | `GET projects` | [docs](https://developers.asana.com/reference/getprojects) |
| [Get multiple tags](actions/get-multiple-tags.md) | `GET tags` | [docs](https://developers.asana.com/reference/gettags) |
| [Get multiple tasks](actions/get-multiple-tasks.md) | `GET tasks` | [docs](https://developers.asana.com/reference/gettasks) |
| [Get multiple users](actions/get-multiple-users.md) | `GET users` | [docs](https://developers.asana.com/reference/getusers) |
| [Get multiple webhooks](actions/get-multiple-webhooks.md) | `GET webhooks` | [docs](https://developers.asana.com/reference/getwebhooks) |
| [Get multiple workspaces](actions/get-multiple-workspaces.md) | `GET workspaces` | [docs](https://developers.asana.com/reference/getworkspaces) |
| [Get objects via typeahead](actions/get-objects-via-typeahead.md) | `GET workspaces/:workspace_gid/typeahead` | [docs](https://developers.asana.com/reference/typeaheadforworkspace) |
| [Get parent goals from a goal](actions/get-parent-goals-from-a-goal.md) | `GET goals/:goal_gid/parentGoals` | [docs](https://developers.asana.com/reference/getparentgoalsforgoal) |
| [Get portfolio items](actions/get-portfolio-items.md) | `GET portfolios/:portfolio_gid/items` | [docs](https://developers.asana.com/reference/getitemsforportfolio) |
| [Get projects a task is in](actions/get-projects-a-task-is-in.md) | `GET tasks/:task_gid/projects` | [docs](https://developers.asana.com/reference/getprojectsfortask) |
| [Get sections in a project](actions/get-sections-in-a-project.md) | `GET projects/:project_gid/sections` | [docs](https://developers.asana.com/reference/getsectionsforproject) |
| [Get status updates from an object](actions/get-status-updates-from-an-object.md) | `GET status_updates` | [docs](https://developers.asana.com/reference/getstatusesforobject) |
| [Get statuses from a project](actions/get-statuses-from-a-project.md) | `GET projects/:project_gid/project_statuses` | [docs](https://developers.asana.com/reference/getprojectstatusesforproject) |
| [Get stories from a task](actions/get-stories-from-a-task.md) | `GET tasks/:task_gid/stories` | [docs](https://developers.asana.com/reference/getstoriesfortask) |
| [Get subtasks from a task](actions/get-subtasks-from-a-task.md) | `GET tasks/:task_gid/subtasks` | [docs](https://developers.asana.com/reference/getsubtasksfortask) |
| [Get tags in a workspace](actions/get-tags-in-a-workspace.md) | `GET workspaces/:workspace_gid/tags` | [docs](https://developers.asana.com/reference/gettagsforworkspace) |
| [Get task count of a project](actions/get-task-count-of-a-project.md) | `GET projects/:project_gid/task_counts` | [docs](https://developers.asana.com/reference/gettaskcountsforproject) |
| [Get tasks from a project](actions/get-tasks-from-a-project.md) | `GET projects/:project_gid/tasks` | [docs](https://developers.asana.com/reference/gettasksforproject) |
| [Get tasks from a section](actions/get-tasks-from-a-section.md) | `GET sections/:section_gid/tasks` | [docs](https://developers.asana.com/reference/gettasksforsection) |
| [Get tasks from a tag](actions/get-tasks-from-a-tag.md) | `GET tags/:tag_gid/tasks` | [docs](https://developers.asana.com/reference/gettasksfortag) |
| [Get tasks from a user task list](actions/get-tasks-from-a-user-task-list.md) | `GET user_task_lists/:user_task_list_gid/tasks` | [docs](https://developers.asana.com/reference/gettasksforusertasklist) |
| [Get team memberships](actions/get-team-memberships.md) | `GET team_memberships` | [docs](https://developers.asana.com/reference/getteammemberships) |
| [Get teams for a user](actions/get-teams-for-a-user.md) | `GET users/:user_gid/teams` | [docs](https://developers.asana.com/reference/getteamsforuser) |
| [Get teams in a workspace](actions/get-teams-in-a-workspace.md) | `GET workspaces/:workspace_gid/teams` | [docs](https://developers.asana.com/reference/getteamsforworkspace) |
| [Get the workspace memberships for a workspace](actions/get-the-workspace-memberships-for-a-workspace.md) | `GET workspaces/:workspace_gid/workspace_memberships` | [docs](https://developers.asana.com/reference/getworkspacemembershipsforworkspace) |
| [Get time periods](actions/get-time-periods.md) | `GET time_periods` | [docs](https://developers.asana.com/reference/gettimeperiods) |
| [Get users in a team](actions/get-users-in-a-team.md) | `GET teams/:team_gid/users` | [docs](https://developers.asana.com/reference/getusersforteam) |
| [Get users in a workspace or organization](actions/get-users-in-a-workspace-or-organization.md) | `GET workspaces/:workspace_gid/users` | [docs](https://developers.asana.com/reference/getusersforworkspace) |
| [Get workspace memberships for a user](actions/get-workspace-memberships-for-a-user.md) | `GET users/:user_gid/workspace_memberships` | [docs](https://developers.asana.com/reference/getworkspacemembershipsforuser) |
| [Instantiate a project from a project template](actions/instantiate-a-project-from-a-project-template.md) | `POST project_templates/:project_template_gid/instantiateProject` | [docs](https://developers.asana.com/reference/instantiateproject) |
| [Move or Insert sections](actions/move-or-insert-sections.md) | `POST projects/:project_gid/sections/insert` | [docs](https://developers.asana.com/reference/insertsectionforproject) |
| [Remove a collaborator from a goal](actions/remove-a-collaborator-from-a-goal.md) | `POST goals/:goal_gid/removeFollowers` | [docs](https://developers.asana.com/reference/removefollowers) |
| [Remove a custom field from a portfolio](actions/remove-a-custom-field-from-a-portfolio.md) | `POST portfolios/:portfolio_gid/removeCustomFieldSetting` | [docs](https://developers.asana.com/reference/removecustomfieldsettingforportfolio) |
| [Remove a custom field from a project](actions/remove-a-custom-field-from-a-project.md) | `POST projects/:project_gid/removeCustomFieldSetting` | [docs](https://developers.asana.com/reference/removecustomfieldsettingforproject) |
| [Remove a portfolio item](actions/remove-a-portfolio-item.md) | `POST portfolios/:portfolio_gid/removeItem` | [docs](https://developers.asana.com/reference/removeitemforportfolio) |
| [Remove a project from a task](actions/remove-a-project-from-a-task.md) | `POST tasks/:task_gid/removeProject` | [docs](https://developers.asana.com/reference/removeprojectfortask) |
| [Remove a tag from a task](actions/remove-a-tag-from-a-task.md) | `POST tasks/:task_gid/removeTag` | [docs](https://developers.asana.com/reference/removetagfortask) |
| [Remove a user from a team](actions/remove-a-user-from-a-team.md) | `POST teams/:team_gid/removeUser` | [docs](https://developers.asana.com/reference/removeuserforteam) |
| [Remove a user from a workspace or organization](actions/remove-a-user-from-a-workspace-or-organization.md) | `POST workspaces/:workspace_gid/removeUser` | [docs](https://developers.asana.com/reference/removeuserforworkspace) |
| [Remove followers from a project](actions/remove-followers-from-a-project.md) | `POST projects/:project_gid/removeFollowers` | [docs](https://developers.asana.com/reference/removefollowersforproject) |
| [Remove followers from a task](actions/remove-followers-from-a-task.md) | `POST tasks/:task_gid/removeFollowers` | [docs](https://developers.asana.com/reference/removefollowerfortask) |
| [Remove users from a portfolio](actions/remove-users-from-a-portfolio.md) | `POST portfolios/:portfolio_gid/removeMembers` | [docs](https://developers.asana.com/reference/removemembersforportfolio) |
| [Remove users from a project](actions/remove-users-from-a-project.md) | `POST projects/:project_gid/removeMembers` | [docs](https://developers.asana.com/reference/removemembersforproject) |
| [Removes a supporting goal relationship](actions/removes-a-supporting-goal-relationship.md) | `POST goals/:goal_gid/removeSupportingRelationship` | [docs](https://developers.asana.com/reference/removesupportingrelationship) |
| [Reorder a custom field's enum](actions/reorder-a-custom-fields-enum.md) | `POST custom_fields/:custom_field_gid/enum_options/insert` | [docs](https://developers.asana.com/reference/insertenumoptionforcustomfield) |
| [Search tasks in a workspace](actions/search-tasks-in-a-workspace.md) | `GET workspaces/:workspace_gid/tasks/search` | [docs](https://developers.asana.com/reference/searchtasksforworkspace) |
| [Set dependencies for a task](actions/set-dependencies-for-a-task.md) | `POST tasks/:task_gid/addDependencies` | [docs](https://developers.asana.com/reference/adddependenciesfortask) |
| [Set dependents for a task](actions/set-dependents-for-a-task.md) | `POST tasks/:task_gid/addDependents` | [docs](https://developers.asana.com/reference/adddependentsfortask) |
| [Set the parent of a task](actions/set-the-parent-of-a-task.md) | `POST tasks/:task_gid/setParent` | [docs](https://developers.asana.com/reference/setparentfortask) |
| [Submit parallel requests](actions/submit-parallel-requests.md) | `POST batch` | [docs](https://developers.asana.com/reference/createbatchrequest) |
| [Unlink dependencies from a task](actions/unlink-dependencies-from-a-task.md) | `POST tasks/:task_gid/removeDependencies` | [docs](https://developers.asana.com/reference/removedependenciesfortask) |
| [Unlink dependents from a task](actions/unlink-dependents-from-a-task.md) | `POST tasks/:task_gid/removeDependents` | [docs](https://developers.asana.com/reference/removedependentsfortask) |
| [Update a custom field](actions/update-a-custom-field.md) | `PUT custom_fields/:custom_field_gid` | [docs](https://developers.asana.com/reference/updatecustomfield) |
| [Update a goal](actions/update-a-goal.md) | `PUT goals/:goal_gid` | [docs](https://developers.asana.com/reference/updategoal) |
| [Update a goal metric](actions/update-a-goal-metric.md) | `POST goals/:goal_gid/setMetricCurrentValue` | [docs](https://developers.asana.com/reference/updategoalmetric) |
| [Update a goal relationship](actions/update-a-goal-relationship.md) | `PUT goal_relationships/:goal_relationship_gid` | [docs](https://developers.asana.com/reference/updategoalrelationship) |
| [Update a portfolio](actions/update-a-portfolio.md) | `PUT portfolios/:portfolio_gid` | [docs](https://developers.asana.com/reference/updateportfolio) |
| [Update a project](actions/update-a-project.md) | `PUT projects/:project_gid` | [docs](https://developers.asana.com/reference/updateproject) |
| [Update a project brief](actions/update-a-project-brief.md) | `PUT project_briefs/:project_brief_gid` | [docs](https://developers.asana.com/reference/updateprojectbrief) |
| [Update a section](actions/update-a-section.md) | `PUT sections/:section_gid` | [docs](https://developers.asana.com/reference/updatesection) |
| [Update a story](actions/update-a-story.md) | `PUT stories/:story_gid` | [docs](https://developers.asana.com/reference/updatestory) |
| [Update a tag](actions/update-a-tag.md) | `PUT tags/:tag_gid` | [docs](https://developers.asana.com/reference/updatetag) |
| [Update a task](actions/update-a-task.md) | `PUT tasks/:task_gid` | [docs](https://developers.asana.com/reference/updatetask) |
| [Update a team](actions/update-a-team.md) | `PUT teams/:team_gid` | [docs](https://developers.asana.com/reference/updateteam) |
| [Update a webhook](actions/update-a-webhook.md) | `PUT webhooks/:webhook_gid` | [docs](https://developers.asana.com/reference/updatewebhook) |
| [Update a workspace](actions/update-a-workspace.md) | `PUT workspaces/:workspace_gid` | [docs](https://developers.asana.com/reference/updateworkspace) |
| [Update an enum option](actions/update-an-enum-option.md) | `PUT enum_options/:enum_option_gid` | [docs](https://developers.asana.com/reference/updateenumoption) |
| [Upload an attachment](actions/upload-an-attachment.md) | `POST attachments` | [docs](https://developers.asana.com/reference/createattachmentforobject) |
