# <img src="https://images.mindcloud.co/apps/icons/asana_1782739178620.png" alt="Asana logo" width="28" height="28"> Asana: Universal API

Connect Asana to read and manage workspaces, projects, tasks, users, and teams through the official Asana REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/asanaNew/latest
- **Category:** Support / Ticketing
- **Actions:** 168
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://asana.com/
- **Vendor API docs:** https://developers.asana.com/reference/rest-api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get multiple workspaces](actions/get-multiple-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-multiple-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (168)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Delete an attachment](actions/delete-an-attachment.md) | DELETE | Deletes an attachment from Asana. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Add a portfolio item](actions/add-a-portfolio-item.md) | POST | Adds an item to a portfolio in Asana. |
| [Add a supporting goal relationship](actions/add-a-supporting-goal-relationship.md) | POST | Adds a supporting goal relationship in Asana. |
| [Create a status update](actions/create-a-status-update.md) | POST | Creates a status update in Asana. |
| [Create an enum option](actions/create-an-enum-option.md) | POST | Creates an enum option in Asana. |
| [Delete a status update](actions/delete-a-status-update.md) | DELETE | Deletes a status update from Asana. |
| [Delete a webhook](actions/delete-a-webhook.md) | DELETE | Deletes a webhook from Asana. |
| [Get a goal](actions/get-a-goal.md) | GET | Retrieves a goal from Asana. |
| [Get a portfolio's custom fields](actions/get-a-portfolios-custom-fields.md) | GET | Retrieves a portfolio's custom fields from Asana. |
| [Get a time period](actions/get-a-time-period.md) | GET | Retrieves a time period from Asana. |
| [Get a workspace membership](actions/get-a-workspace-membership.md) | GET | Retrieves a workspace membership from Asana. |
| [Get a workspace's custom fields](actions/get-a-workspaces-custom-fields.md) | GET | Retrieves a workspace's custom fields from Asana. |
| [Get events on a resource](actions/get-events-on-a-resource.md) | GET | Retrieves events for a resource from Asana. |
| [Get multiple portfolio memberships](actions/get-multiple-portfolio-memberships.md) | GET | Retrieves portfolio memberships from Asana. |
| [Get teams in a workspace](actions/get-teams-in-a-workspace.md) | GET | Retrieves teams in an Asana workspace. |
| [Remove a user from a workspace or organization](actions/remove-a-user-from-a-workspace-or-organization.md) | POST | Removes a user from an Asana workspace or organization. |
| [Remove users from a portfolio](actions/remove-users-from-a-portfolio.md) | POST | Removes users from an Asana portfolio. |
| [Search tasks in a workspace](actions/search-tasks-in-a-workspace.md) | GET | Finds tasks in an Asana workspace. |
| [Update a goal metric](actions/update-a-goal-metric.md) | POST | Updates a goal metric in Asana. |
| [Update a goal relationship](actions/update-a-goal-relationship.md) | PUT | Updates a goal relationship in Asana. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add a collaborator to a goal](actions/add-a-collaborator-to-a-goal.md) | PUT | Adds a collaborator to a goal in Asana. |
| [Add a custom field to a portfolio](actions/add-a-custom-field-to-a-portfolio.md) | PUT | Adds a custom field to a portfolio in Asana. |
| [Add a custom field to a project](actions/add-a-custom-field-to-a-project.md) | PUT | Adds a custom field to a project in Asana. |
| [Add a project to a task](actions/add-a-project-to-a-task.md) | POST | Adds a project to a task in Asana. |
| [Add a tag to a task](actions/add-a-tag-to-a-task.md) | PUT | Adds a tag to a task in Asana. |
| [Add a user to a team](actions/add-a-user-to-a-team.md) | POST | Adds a user to a team in Asana. |
| [Add a user to a workspace or organization](actions/add-a-user-to-a-workspace-or-organization.md) | POST | Adds a user to an Asana workspace or organization. |
| [Add followers to a task](actions/add-followers-to-a-task.md) | POST | Adds followers to a task in Asana. |
| [Add task to section](actions/add-task-to-section.md) | PUT | Adds a task to a section in Asana. |
| [Add users to a portfolio](actions/add-users-to-a-portfolio.md) | POST | Adds users to a portfolio in Asana. |
| [Add users to a project](actions/add-users-to-a-project.md) | POST | Adds users to a project in Asana. |
| [Create a custom field](actions/create-a-custom-field.md) | POST | Creates a custom field in Asana. |
| [Create a goal](actions/create-a-goal.md) | POST | Creates a goal in Asana. |
| [Create a goal metric](actions/create-a-goal-metric.md) | PUT | Creates a goal metric in Asana. |
| [Create a membership](actions/create-a-membership.md) | POST | Creates a membership for an object in Asana. |
| [Create a portfolio](actions/create-a-portfolio.md) | POST | Creates a portfolio in Asana. |
| [Create a project](actions/create-a-project.md) | POST | Creates a project in Asana. |
| [Create a project brief](actions/create-a-project-brief.md) | POST | Creates a project brief in Asana. |
| [Create a project in a team](actions/create-a-project-in-a-team.md) | POST | Creates a project in an Asana team. |
| [Create a project in a workspace](actions/create-a-project-in-a-workspace.md) | POST | Creates a project in an Asana workspace. |
| [Create a section in a project](actions/create-a-section-in-a-project.md) | POST | Creates a section in a project in Asana. |
| [Create a story on a task](actions/create-a-story-on-a-task.md) | POST | Creates a story on a task in Asana. |
| [Create a tag](actions/create-a-tag.md) | POST | Creates a tag in Asana. |
| [Create a tag in a workspace](actions/create-a-tag-in-a-workspace.md) | POST | Creates a tag in an Asana workspace. |
| [Create a task](actions/create-a-task.md) | POST | Creates a task in Asana. |
| [Create a team](actions/create-a-team.md) | POST | Creates a team in Asana. |
| [Create an organization export request](actions/create-an-organization-export-request.md) | POST | Creates an organization export request in Asana. |
| [Delete a custom field](actions/delete-a-custom-field.md) | DELETE | Deletes a custom field from Asana. |
| [Delete a goal](actions/delete-a-goal.md) | DELETE | Deletes a goal from Asana. |
| [Delete a portfolio](actions/delete-a-portfolio.md) | DELETE | Deletes a portfolio from Asana. |
| [Delete a project](actions/delete-a-project.md) | DELETE | Deletes a project from Asana. |
| [Delete a project status](actions/delete-a-project-status.md) | DELETE | Deletes a project status from Asana. |
| [Delete a section](actions/delete-a-section.md) | DELETE | Deletes a section from Asana. |
| [Delete a story](actions/delete-a-story.md) | DELETE | Deletes a story from Asana. |
| [Delete a tag](actions/delete-a-tag.md) | DELETE | Deletes a tag from Asana. |
| [Delete a task](actions/delete-a-task.md) | DELETE | Deletes a task from Asana. |
| [Duplicate a project](actions/duplicate-a-project.md) | POST | Duplicates a project in Asana. |
| [Establish a webhook](actions/establish-a-webhook.md) | POST | Creates a webhook in Asana. |
| [Get a custom field](actions/get-a-custom-field.md) | GET | Retrieves a custom field from Asana. |
| [Get a goal relationship](actions/get-a-goal-relationship.md) | GET | Retrieves a goal relationship from Asana. |
| [Get a job by id](actions/get-a-job-by-id.md) | GET | Retrieves a job from Asana. |
| [Get a portfolio](actions/get-a-portfolio.md) | GET | Retrieves a portfolio from Asana. |
| [Get a portfolio membership](actions/get-a-portfolio-membership.md) | GET | Retrieves a portfolio membership from Asana. |
| [Get a project](actions/get-a-project.md) | GET | Retrieves a project from Asana. |
| [Get a project brief](actions/get-a-project-brief.md) | GET | Retrieves a project brief from Asana. |
| [Get a project status](actions/get-a-project-status.md) | GET | Retrieves a project status from Asana. |
| [Get a project template](actions/get-a-project-template.md) | GET | Retrieves a project template from Asana. |
| [Get a project's custom fields](actions/get-a-projects-custom-fields.md) | GET | Retrieves a project's custom fields from Asana. |
| [Get a status update](actions/get-a-status-update.md) | GET | Retrieves a status update from Asana. |
| [Get a tag](actions/get-a-tag.md) | GET | Retrieves a tag from Asana. |
| [Get a task](actions/get-a-task.md) | GET | Retrieves a task from Asana. |
| [Get a task's tags](actions/get-a-tasks-tags.md) | GET | Retrieves a task's tags from Asana. |
| [Get a team](actions/get-a-team.md) | GET | Retrieves a team from Asana. |
| [Get a team membership](actions/get-a-team-membership.md) | GET | Retrieves a team membership from Asana. |
| [Get a team's project templates](actions/get-a-teams-project-templates.md) | GET | Retrieves a team's project templates from Asana. |
| [Get a user task list](actions/get-a-user-task-list.md) | GET | Retrieves a user task list from Asana. |
| [Get a user's favorites](actions/get-a-users-favorites.md) | GET | Retrieves a user's favorites from Asana. |
| [Get a webhook](actions/get-a-webhook.md) | GET | Retrieves a webhook from Asana. |
| [Get a workspace](actions/get-a-workspace.md) | GET | Retrieves a workspace from Asana. |
| [Get all projects in a workspace](actions/get-all-projects-in-a-workspace.md) | GET | Retrieves all projects in an Asana workspace. |
| [Get an attachment](actions/get-an-attachment.md) | GET | Retrieves an attachment from Asana. |
| [Get attachments from an object](actions/get-attachments-from-an-object.md) | GET | Retrieves attachments for an object from Asana. |
| [Get audit log events](actions/get-audit-log-events.md) | GET | Retrieves audit log events from Asana. |
| [Get dependencies from a task](actions/get-dependencies-from-a-task.md) | GET | Retrieves dependencies for a task from Asana. |
| [Get dependents from a task](actions/get-dependents-from-a-task.md) | GET | Retrieves dependents for a task from Asana. |
| [Get details on an org export request](actions/get-details-on-an-org-export-request.md) | GET | Retrieves an organization export request from Asana. |
| [Get goal relationships](actions/get-goal-relationships.md) | GET | Retrieves goal relationships from Asana. |
| [Get goals](actions/get-goals.md) | GET | Retrieves goals from Asana. |
| [Get memberships from a portfolio](actions/get-memberships-from-a-portfolio.md) | GET | Retrieves portfolio memberships from Asana. |
| [Get memberships from a project](actions/get-memberships-from-a-project.md) | GET | Retrieves project memberships from Asana. |
| [Get memberships from a team](actions/get-memberships-from-a-team.md) | GET | Retrieves team memberships from Asana. |
| [Get memberships from a user](actions/get-memberships-from-a-user.md) | GET | Retrieves team memberships for a user from Asana. |
| [Get multiple portfolios](actions/get-multiple-portfolios.md) | GET | Retrieves portfolios from Asana. |
| [Get multiple project templates](actions/get-multiple-project-templates.md) | GET | Retrieves project templates from Asana. |
| [Get multiple tags](actions/get-multiple-tags.md) | GET | Retrieves tags from Asana. |
| [Get multiple users](actions/get-multiple-users.md) | GET | Retrieves users from Asana. |
| [Get multiple webhooks](actions/get-multiple-webhooks.md) | GET | Retrieves webhooks from Asana. |
| [Get objects via typeahead](actions/get-objects-via-typeahead.md) | GET | Finds objects in Asana by typeahead. |
| [Get parent goals from a goal](actions/get-parent-goals-from-a-goal.md) | GET | Retrieves parent goals for a goal from Asana. |
| [Get portfolio items](actions/get-portfolio-items.md) | GET | Retrieves portfolio items from Asana. |
| [Get projects a task is in](actions/get-projects-a-task-is-in.md) | GET | Retrieves the projects for a task from Asana. |
| [Get status updates from an object](actions/get-status-updates-from-an-object.md) | GET | Retrieves status updates for an object from Asana. |
| [Get statuses from a project](actions/get-statuses-from-a-project.md) | GET | Retrieves project statuses from Asana. |
| [Get subtasks from a task](actions/get-subtasks-from-a-task.md) | GET | Retrieves subtasks for a task from Asana. |
| [Get tags in a workspace](actions/get-tags-in-a-workspace.md) | GET | Retrieves tags in an Asana workspace. |
| [Get task count of a project](actions/get-task-count-of-a-project.md) | GET | Retrieves a project's task count from Asana. |
| [Get tasks from a section](actions/get-tasks-from-a-section.md) | GET | Retrieves tasks from a section in Asana. |
| [Get tasks from a tag](actions/get-tasks-from-a-tag.md) | GET | Retrieves tasks from a tag in Asana. |
| [Get tasks from a user task list](actions/get-tasks-from-a-user-task-list.md) | GET | Retrieves tasks from a user task list in Asana. |
| [Get teams for a user](actions/get-teams-for-a-user.md) | GET | Retrieves teams for a user from Asana. |
| [Get the workspace memberships for a workspace](actions/get-the-workspace-memberships-for-a-workspace.md) | GET | Retrieves workspace memberships for a workspace from Asana. |
| [Get time periods](actions/get-time-periods.md) | GET | Retrieves time periods from Asana. |
| [Get users in a team](actions/get-users-in-a-team.md) | GET | Retrieves users in an Asana team. |
| [Get users in a workspace or organization](actions/get-users-in-a-workspace-or-organization.md) | GET | Retrieves users in an Asana workspace or organization. |
| [Get workspace memberships for a user](actions/get-workspace-memberships-for-a-user.md) | GET | Retrieves a user's workspace memberships from Asana. |
| [Instantiate a project from a project template](actions/instantiate-a-project-from-a-project-template.md) | POST | Creates a project from an Asana project template. |
| [Move or Insert sections](actions/move-or-insert-sections.md) | POST | Moves or inserts sections in an Asana project. |
| [Remove a collaborator from a goal](actions/remove-a-collaborator-from-a-goal.md) | POST | Removes a collaborator from a goal in Asana. |
| [Remove a custom field from a portfolio](actions/remove-a-custom-field-from-a-portfolio.md) | POST | Removes a custom field from a portfolio in Asana. |
| [Remove a custom field from a project](actions/remove-a-custom-field-from-a-project.md) | POST | Removes a custom field from a project in Asana. |
| [Remove a portfolio item](actions/remove-a-portfolio-item.md) | PUT | Removes an item from an Asana portfolio. |
| [Remove a tag from a task](actions/remove-a-tag-from-a-task.md) | POST | Removes a tag from a task in Asana. |
| [Remove followers from a project](actions/remove-followers-from-a-project.md) | POST | Removes followers from a project in Asana. |
| [Remove followers from a task](actions/remove-followers-from-a-task.md) | PUT | Removes followers from a task in Asana. |
| [Remove users from a project](actions/remove-users-from-a-project.md) | PUT | Removes users from a project in Asana. |
| [Removes a supporting goal relationship](actions/removes-a-supporting-goal-relationship.md) | POST | Removes a supporting goal relationship in Asana. |
| [Reorder a custom field's enum](actions/reorder-a-custom-fields-enum.md) | POST | Reorders a custom field's enum options in Asana. |
| [Set dependencies for a task](actions/set-dependencies-for-a-task.md) | PUT | Sets dependencies for a task in Asana. |
| [Set the parent of a task](actions/set-the-parent-of-a-task.md) | POST | Sets a task's parent in Asana. |
| [Submit parallel requests](actions/submit-parallel-requests.md) | POST | Submits parallel API requests to Asana. |
| [Unlink dependencies from a task](actions/unlink-dependencies-from-a-task.md) | POST | Removes dependencies from a task in Asana. |
| [Unlink dependents from a task](actions/unlink-dependents-from-a-task.md) | POST | Removes dependents from a task in Asana. |
| [Update a custom field](actions/update-a-custom-field.md) | PUT | Updates a custom field in Asana. |
| [Update a goal](actions/update-a-goal.md) | PUT | Updates a goal in Asana. |
| [Update a portfolio](actions/update-a-portfolio.md) | PUT | Updates a portfolio in Asana. |
| [Update a project brief](actions/update-a-project-brief.md) | PUT | Updates a project brief in Asana. |
| [Update a section](actions/update-a-section.md) | PUT | Updates a section in Asana. |
| [Update a story](actions/update-a-story.md) | PUT | Updates a story in Asana. |
| [Update a tag](actions/update-a-tag.md) | PUT | Updates a tag in Asana. |
| [Update a team](actions/update-a-team.md) | PUT | Updates a team in Asana. |
| [Update a webhook](actions/update-a-webhook.md) | PUT | Updates a webhook in Asana. |
| [Update a workspace](actions/update-a-workspace.md) | PUT | Updates a workspace in Asana. |
| [Update an enum option](actions/update-an-enum-option.md) | PUT | Updates an enum option in Asana. |
| [Upload an attachment](actions/upload-an-attachment.md) | POST | Uploads an attachment to an object in Asana. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Add followers to a project](actions/add-followers-to-a-project.md) | POST | Adds followers to a project in Asana. |
| [Create a project status](actions/create-a-project-status.md) | POST | Creates a project status in Asana. |
| [Create a project template from a project](actions/create-a-project-template-from-a-project.md) | POST | Creates a project template from a project in Asana. |
| [Delete a project brief](actions/delete-a-project-brief.md) | DELETE | Deletes a project brief from Asana. |
| [Get a project membership](actions/get-a-project-membership.md) | GET | Retrieves a project membership from Asana. |
| [Get multiple projects](actions/get-multiple-projects.md) | GET | Retrieves projects from Asana. |
| [Get sections in a project](actions/get-sections-in-a-project.md) | GET | Retrieves sections in a project from Asana. |
| [Get tasks from a project](actions/get-tasks-from-a-project.md) | GET | Retrieves tasks from a project in Asana. |
| [Update a project](actions/update-a-project.md) | PUT | Updates a project in Asana. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create a subtask](actions/create-a-subtask.md) | POST | Creates a subtask in Asana. |
| [Duplicate a task](actions/duplicate-a-task.md) | POST | Duplicates a task in Asana. |
| [Get a section](actions/get-a-section.md) | GET | Retrieves a section from Asana. |
| [Get a story](actions/get-a-story.md) | GET | Retrieves a story from Asana. |
| [Get multiple tasks](actions/get-multiple-tasks.md) | GET | Retrieves tasks from Asana. |
| [Get stories from a task](actions/get-stories-from-a-task.md) | GET | Retrieves stories for a task from Asana. |
| [Remove a project from a task](actions/remove-a-project-from-a-task.md) | POST | Removes a project from a task in Asana. |
| [Set dependents for a task](actions/set-dependents-for-a-task.md) | POST | Sets dependents for a task in Asana. |
| [Update a task](actions/update-a-task.md) | PUT | Updates a task in Asana. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get a team's projects](actions/get-a-teams-projects.md) | GET | Retrieves a team's projects from Asana. |
| [Get team memberships](actions/get-team-memberships.md) | GET | Retrieves team memberships from Asana. |
| [Remove a user from a team](actions/remove-a-user-from-a-team.md) | POST | Removes a user from a team in Asana. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get multiple workspaces](actions/get-multiple-workspaces.md) | GET | Retrieves workspaces from Asana. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get a user](actions/get-a-user.md) | GET | Retrieves a user from Asana. |
| [Get a user's task list](actions/get-a-users-task-list.md) | GET | Retrieves a user's task list from Asana. |

