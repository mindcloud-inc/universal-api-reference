# <img src="https://images.mindcloud.co/apps/icons/easy-redmine_1776187550757.png" alt="Easy Redmine logo" width="28" height="28"> Easy Redmine: Universal API

Manage Easy Redmine projects, tasks, users, groups, time entries, memberships, and search through the Easy8 REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyRedmine/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.easyredmine.com
- **Vendor API docs:** https://www.easy8.com/documentation-of-easy8/article/rest-api-specification

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Custom Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Field](actions/get-custom-field.md) | GET | Retrieves a custom field from Easy Redmine. |
| [List Custom Fields](actions/list-custom-fields.md) | GET | Retrieves custom fields from Easy Redmine. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Easy Redmine. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Easy Redmine. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Easy Redmine. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Easy Redmine. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Easy Redmine. |

### Group Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Group](actions/add-user-to-group.md) | PUT | Adds a user to a group in Easy Redmine. |
| [Remove User From Group](actions/remove-user-from-group.md) | DELETE | Removes a user from a group in Easy Redmine. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Add Issue To Favorites](actions/add-issue-to-favorites.md) | PUT | Adds an issue to favorites in Easy Redmine. |
| [Add Issue Watcher](actions/add-issue-watcher.md) | PUT | Adds a watcher to an issue in Easy Redmine. |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in Easy Redmine. |
| [Delete Issue](actions/delete-issue.md) | DELETE | Deletes an existing issue from Easy Redmine. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an issue from Easy Redmine. |
| [List Issues](actions/list-issues.md) | GET | Retrieves issues from Easy Redmine. |
| [Remove Issue From Favorites](actions/remove-issue-from-favorites.md) | PUT | Removes an issue from favorites in Easy Redmine. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in Easy Redmine. |

### Issue Watcher

| Action | Method | Description |
| --- | --- | --- |
| [Remove Issue Watcher](actions/remove-issue-watcher.md) | DELETE | Removes a watcher from an issue in Easy Redmine. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Add Project To Favorites](actions/add-project-to-favorites.md) | PUT | Adds a project to favorites in Easy Redmine. |
| [Archive Project](actions/archive-project.md) | PUT | Archives an existing project in Easy Redmine. |
| [Close Project](actions/close-project.md) | PUT | Closes an existing project in Easy Redmine. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Easy Redmine. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Easy Redmine. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Easy Redmine. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Easy Redmine. |
| [Remove Project From Favorites](actions/remove-project-from-favorites.md) | PUT | Removes a project from favorites in Easy Redmine. |
| [Reopen Project](actions/reopen-project.md) | PUT | Reopens an existing project in Easy Redmine. |
| [Unarchive Project](actions/unarchive-project.md) | PUT | Unarchives an existing project in Easy Redmine. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Easy Redmine. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Searches for records across Easy Redmine. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Easy Redmine. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from Easy Redmine. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from Easy Redmine. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Easy Redmine. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Easy Redmine. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [Create Version](actions/create-version.md) | POST | Creates a new version in an Easy Redmine project. |
| [Delete Version](actions/delete-version.md) | DELETE | Deletes an existing version from Easy Redmine. |
| [Get Version](actions/get-version.md) | GET | Retrieves a version from Easy Redmine. |
| [List Versions](actions/list-versions.md) | GET | Retrieves versions from Easy Redmine. |
| [Update Version](actions/update-version.md) | PUT | Updates an existing version in Easy Redmine. |

