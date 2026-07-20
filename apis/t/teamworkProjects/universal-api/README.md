# <img src="https://images.mindcloud.co/apps/icons/teamwork-projects_1778006152702.png" alt="Teamwork Projects logo" width="28" height="28"> Teamwork Projects: Universal API

Connect to Teamwork.com Projects to read and manage projects, tasks, task lists, milestones, comments, people, companies, tags, time entries, project updates, and related project work records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/teamworkProjects/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.teamwork.com/
- **Vendor API docs:** https://apidocs.teamwork.com/docs/teamwork

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Project Task List Report](actions/generate-project-task-list-report.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/generate-project-task-list-report?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Comments](actions/list-comments.md) | GET | Retrieves all comments from Teamwork Projects. |
| [List Task Comments](actions/list-task-comments.md) | GET | Retrieves comments for a task from Teamwork Projects. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves all companies from Teamwork Projects. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves all messages from Teamwork Projects. |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [List Milestones](actions/list-milestones.md) | GET | Retrieves all milestones from Teamwork Projects. |

### Notebook

| Action | Method | Description |
| --- | --- | --- |
| [Get Notebook](actions/get-notebook.md) | GET | Retrieves detailed notebook information from Teamwork Projects. |
| [List Notebooks](actions/list-notebooks.md) | GET | Retrieves all notebooks from Teamwork Projects. |

### Notebook Version

| Action | Method | Description |
| --- | --- | --- |
| [List Notebook Versions](actions/list-notebook-versions.md) | GET | Retrieves notebook versions from Teamwork Projects. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [List People](actions/list-people.md) | GET | Retrieves all people from Teamwork Projects. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves detailed project information from Teamwork Projects. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all projects from Teamwork Projects. |
| [List Sample Projects](actions/list-sample-projects.md) | GET | Retrieves sample projects from Teamwork Projects. |

### Project Task List Report

| Action | Method | Description |
| --- | --- | --- |
| [Generate Project Task List Report](actions/generate-project-task-list-report.md) | GET | Generates a project task list report in Teamwork Projects. |

### Project Update

| Action | Method | Description |
| --- | --- | --- |
| [List Project Updates](actions/list-project-updates.md) | GET | Retrieves project updates from Teamwork Projects. |

### Risk

| Action | Method | Description |
| --- | --- | --- |
| [List Project Risks](actions/list-project-risks.md) | GET | Retrieves project risks from Teamwork Projects. |

### Skill

| Action | Method | Description |
| --- | --- | --- |
| [List Skills](actions/list-skills.md) | GET | Retrieves all skills from Teamwork Projects. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves all tags from Teamwork Projects. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves detailed task information from Teamwork Projects. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves tasks for a project from Teamwork Projects. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves all tasks from Teamwork Projects. |

### Task List

| Action | Method | Description |
| --- | --- | --- |
| [List Task Lists](actions/list-task-lists.md) | GET | Retrieves task lists from Teamwork Projects. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Task Time Entries](actions/list-task-time-entries.md) | GET | Retrieves time entries for a task from Teamwork Projects. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Teamwork Projects. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves all timesheets from Teamwork Projects. |

