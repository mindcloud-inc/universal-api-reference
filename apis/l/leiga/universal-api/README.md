# <img src="https://images.mindcloud.co/apps/icons/images_1775504454039.jpeg" alt="Leiga logo" width="28" height="28"> Leiga: Universal API

Leiga is an AI-powered project management platform for projects, issues, sprints, workflows, comments, and related team operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leiga/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.leiga.com
- **Vendor API docs:** https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leiga/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Leiga. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from Leiga for an issue. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Leiga. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Leiga by project ID. |
| [Get Project by Project Key](actions/get-project-by-project-key.md) | GET | Retrieves a project from Leiga by project key. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from Leiga. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Leiga. |

### Sprints

| Action | Method | Description |
| --- | --- | --- |
| [Create Sprint](actions/create-sprint.md) | POST | Creates a new sprint in Leiga. |
| [Get Sprint](actions/get-sprint.md) | GET | Retrieves detailed sprint information from Leiga. |
| [List Project Sprints](actions/list-project-sprints.md) | GET | Retrieves sprints for a project in Leiga. |
| [Update Sprint](actions/update-sprint.md) | PUT | Updates an existing sprint in Leiga. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List State Transitions](actions/list-state-transitions.md) | GET | Retrieves available state transitions from Leiga. |

### Subtasks

| Action | Method | Description |
| --- | --- | --- |
| [Batch Add Subtasks](actions/batch-add-subtasks.md) | POST | Creates multiple new subtasks in Leiga. |
| [List Subtasks](actions/list-subtasks.md) | GET | Retrieves subtasks from Leiga for an issue. |
| [Remove Subtask](actions/remove-subtask.md) | DELETE | Deletes an existing subtask from Leiga. |
| [Update Subtask](actions/update-subtask.md) | PUT | Updates an existing subtask in Leiga. |
| [Update Subtask Status](actions/update-subtask-status.md) | PUT | Updates a subtask status in Leiga. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Add Issue Relation](actions/add-issue-relation.md) | POST | Creates an issue relation in Leiga. |
| [Batch Add Issue](actions/batch-add-issue.md) | POST | Creates multiple new issues in Leiga. |
| [Batch Update Issue](actions/batch-update-issue.md) | PUT | Updates multiple existing issues in Leiga. |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in Leiga. |
| [Get Issue by Issue Number](actions/get-issue-by-issue-number.md) | GET | Retrieves an issue from Leiga by issue number. |
| [Get Issue Detail V2](actions/get-issue-detail-v2.md) | GET | Retrieves detailed issue information from Leiga. |
| [Get Issue Field Detail](actions/get-issue-field-detail.md) | GET | Retrieves issue field details from Leiga. |
| [Get Issue Scheme](actions/get-issue-scheme.md) | GET | Retrieves an issue scheme from Leiga. |
| [List Issue Fields](actions/list-issue-fields.md) | GET | Retrieves a list of issue fields from Leiga. |
| [List Issue Relations](actions/list-issue-relations.md) | GET | Retrieves issue relations for an issue in Leiga. |
| [List Issue Select Options](actions/list-issue-select-options.md) | GET | Retrieves selectable issue field options from Leiga. |
| [List Issue Types](actions/list-issue-types.md) | GET | Retrieves a list of issue types from Leiga. |
| [List Project Issue Filter Fields](actions/list-project-issue-filter-fields.md) | GET | Retrieves issue filter fields for a project in Leiga. |
| [Remove Issue](actions/remove-issue.md) | DELETE | Deletes an existing issue from Leiga. |
| [Remove Issue Relation](actions/remove-issue-relation.md) | DELETE | Deletes an existing issue relation from Leiga. |
| [Search Issues](actions/search-issues.md) | GET | Finds issues in Leiga using paginated project filters. |
| [Search Issues V2](actions/search-issues-v2.md) | GET | Finds issues in Leiga using structured project filters. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in Leiga. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Add Project Members](actions/add-project-members.md) | POST | Adds members to a project in Leiga. |
| [List Project Members](actions/list-project-members.md) | GET | Retrieves project members from Leiga with pagination. |
| [Remove Project Members](actions/remove-project-members.md) | DELETE | Removes members from a project in Leiga. |
| [Update Project Member Roles](actions/update-project-member-roles.md) | PUT | Updates project member roles in Leiga. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Project Workflows](actions/list-project-workflows.md) | GET | Retrieves workflows for a project in Leiga. |

