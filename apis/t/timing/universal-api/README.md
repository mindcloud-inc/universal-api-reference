# <img src="https://images.mindcloud.co/apps/icons/timing_1774011668755.png" alt="Timing logo" width="28" height="28"> Timing: Universal API

Automatic time tracking and reporting for Mac teams and individuals through the Timing Web API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timing/latest
- **Category:** Productivity / Project Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://timingapp.com
- **Vendor API docs:** https://web.timingapp.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timing/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity Hierarchy](actions/get-activity-hierarchy.md) | GET | Retrieves the activity hierarchy from Timing. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Timing. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes a project and its children from Timing. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all project records from Timing. |
| [List Projects Hierarchically](actions/list-projects-hierarchically.md) | GET | Retrieves the complete project hierarchy from Timing. |
| [Show Project](actions/show-project.md) | GET | Retrieves a specific project from Timing. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Timing. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Generate Report](actions/generate-report.md) | GET | Retrieves a time and app usage report from Timing. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET | Retrieves all team records from Timing. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Batch Update Time Entries](actions/batch-update-time-entries.md) | PUT | Updates multiple time entries at once in Timing. |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Timing. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from Timing. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves all time entries from Timing. |
| [Show Latest Time Entry](actions/show-latest-time-entry.md) | GET | Retrieves the latest time entry from Timing. |
| [Show Running Timer](actions/show-running-timer.md) | GET | Retrieves the currently running time entry from Timing. |
| [Show Time Entry](actions/show-time-entry.md) | GET | Retrieves a time entry from Timing. |
| [Start Timer](actions/start-timer.md) | POST | Starts a new timer in Timing, stopping any running timer. |
| [Stop Timer](actions/stop-timer.md) | PUT | Stops the currently running timer in Timing. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Timing. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves active team members from Timing. |

