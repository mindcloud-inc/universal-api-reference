# <img src="https://images.mindcloud.co/apps/icons/timely_1774893805269.png" alt="Timely logo" width="28" height="28"> Timely: Universal API

The Timely API allows you to integrate time tracking into your applications and workflows. Use it to sync projects, log time entries, export reports, and automate time management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timely/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.timely.com
- **Vendor API docs:** https://developer.timely.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Token Info](actions/get-current-token-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/get-current-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Token Info](actions/get-current-token-info.md) | GET | Retrieves details about the current OAuth access token from Timely. |

### Client Company

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a client in Timely. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Timely. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Timely. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Timely. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in Timely. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Timely. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Timely. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Timely. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Timely. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Filter Reports](actions/filter-reports.md) | GET | Retrieves filtered reports from Timely. |
| [Get Report Totals](actions/get-report-totals.md) | GET | Retrieves report totals from Timely. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a tag in Timely. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from Timely. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Timely. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Timely. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in Timely. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a task in Timely. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Timely. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Timely. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Timely. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Timely. |

### Task Summary Report

| Action | Method | Description |
| --- | --- | --- |
| [List Task Summaries](actions/list-task-summaries.md) | GET | Retrieves task summaries from Timely. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a time entry in Timely. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from Timely. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from Timely. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Timely. |
| [Start Time Entry Timer](actions/start-time-entry-timer.md) | PUT | Starts the timer for an existing time entry in Timely. |
| [Stop Time Entry Timer](actions/stop-time-entry-timer.md) | PUT | Stops the timer for an existing time entry in Timely. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Timely. |

### Time Entry Import Job

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Import Time Entries](actions/bulk-import-time-entries.md) | POST | Creates a bulk import job for time entries in Timely. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Timely. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Timely. |
| [Invite User](actions/invite-user.md) | POST | Invites a user to Timely. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Timely. |
| [Search Users](actions/search-users.md) | GET | Finds users in Timely. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Timely. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Timely. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Timely. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Timely. |

