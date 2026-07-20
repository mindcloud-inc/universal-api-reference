# <img src="https://images.mindcloud.co/apps/icons/amazing-marvin_1773833262277.png" alt="Amazing Marvin logo" width="28" height="28"> Amazing Marvin: Universal API

Plan tasks, track habits, and manage goals with Marvin

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/amazingMarvin/latest
- **Category:** Productivity / Project Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://amazingmarvin.com
- **Vendor API docs:** https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Credentials](actions/test-credentials.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/test-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves all categories from Amazing Marvin. |

### Child Items

| Action | Method | Description |
| --- | --- | --- |
| [List Child Items](actions/list-child-items.md) | GET | Retrieves open child tasks and projects from Amazing Marvin. |

### Credential Test

| Action | Method | Description |
| --- | --- | --- |
| [Test Credentials](actions/test-credentials.md) | GET | Tests API credentials in Amazing Marvin. |

### Due Items

| Action | Method | Description |
| --- | --- | --- |
| [List Due Items](actions/list-due-items.md) | GET | Retrieves open due tasks and projects from Amazing Marvin. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates an event in Amazing Marvin. |

### Goals

| Action | Method | Description |
| --- | --- | --- |
| [List Goals](actions/list-goals.md) | GET | Retrieves goals from Amazing Marvin. |

### Habit

| Action | Method | Description |
| --- | --- | --- |
| [Get Habit](actions/get-habit.md) | GET | Retrieves a habit and its history from Amazing Marvin. |
| [Update Habit](actions/update-habit.md) | PUT | Updates habit history in Amazing Marvin. |

### Habits

| Action | Method | Description |
| --- | --- | --- |
| [List Habits](actions/list-habits.md) | GET | Retrieves habits and their history from Amazing Marvin. |

### Kudos

| Action | Method | Description |
| --- | --- | --- |
| [Get Kudos](actions/get-kudos.md) | GET | Retrieves kudos information from Amazing Marvin. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves all labels from Amazing Marvin. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in Amazing Marvin. |

### Reminder

| Action | Method | Description |
| --- | --- | --- |
| [Delete Reminders](actions/delete-reminders.md) | DELETE | Deletes reminders from Amazing Marvin. |
| [Set Reminders](actions/set-reminders.md) | PUT | Sets one or more reminders in Amazing Marvin. |

### Reward Points

| Action | Method | Description |
| --- | --- | --- |
| [Claim Reward Points](actions/claim-reward-points.md) | PUT | Claims reward points in Amazing Marvin. |
| [Spend Reward Points](actions/spend-reward-points.md) | PUT | Spends reward points in Amazing Marvin. |
| [Unclaim Reward Points](actions/unclaim-reward-points.md) | PUT | Unclaims reward points in Amazing Marvin. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a task in Amazing Marvin. |
| [Get Tracked Task](actions/get-tracked-task.md) | GET | Retrieves the tracked task from Amazing Marvin. |
| [Mark Task Done](actions/mark-task-done.md) | PUT | Marks a task done in Amazing Marvin. |
| [Track Task Time](actions/track-task-time.md) | PUT | Starts or stops task time tracking in Amazing Marvin. |

### Task Time Tracks

| Action | Method | Description |
| --- | --- | --- |
| [List Task Time Tracks](actions/list-task-time-tracks.md) | GET | Retrieves task time tracks from Amazing Marvin. |

### Time Blocks

| Action | Method | Description |
| --- | --- | --- |
| [List Today Time Blocks](actions/list-today-time-blocks.md) | GET | Retrieves today's time blocks from Amazing Marvin. |

### Today Items

| Action | Method | Description |
| --- | --- | --- |
| [List Today Items](actions/list-today-items.md) | GET | Retrieves today's scheduled items from Amazing Marvin. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves account information from Amazing Marvin. |

