# Amazing Marvin: Native API Reference

A consolidated summary of Amazing Marvin's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API
- **OpenAPI specification:** https://raw.githubusercontent.com/amazingmarvin/MarvinAPI/master/marvin-api.yaml
- **API base URL:** `https://serv.amazingmarvin.com/api`

## Authentication

### API Key

Connect with an Amazing Marvin API token from the API strategy settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#credentials)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Claim Reward Points](actions/claim-reward-points.md) | `POST /claimRewardPoints` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#claiming-reward-points) |
| [Create Event](actions/create-event.md) | `POST /addEvent` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#create-an-event) |
| [Create Project](actions/create-project.md) | `POST /addProject` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#create-a-project) |
| [Create Task](actions/create-task.md) | `POST /addTask` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#create-a-task) |
| [Delete Reminders](actions/delete-reminders.md) | `POST /reminder/delete` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#delete-one-or-more-reminders) |
| [Get Account Information](actions/get-account-information.md) | `GET /me` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#me) |
| [Get Habit](actions/get-habit.md) | `GET /habit` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-a-habit) |
| [Get Kudos](actions/get-kudos.md) | `GET /kudos` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-marvin-kudos-info) |
| [Get Tracked Task](actions/get-tracked-task.md) | `GET /trackedItem` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-the-currently-tracked-task) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-a-list-of-all-categories) |
| [List Child Items](actions/list-child-items.md) | `GET /children` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-child-tasksprojects-of-a-categoryproject) |
| [List Due Items](actions/list-due-items.md) | `GET /dueItems` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-open-tasks-and-projects-that-are-due-today-or-earlier) |
| [List Goals](actions/list-goals.md) | `GET /goals` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-goals) |
| [List Habits](actions/list-habits.md) | `GET /habits` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#list-habits) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-a-list-of-all-labels) |
| [List Task Time Tracks](actions/list-task-time-tracks.md) | `POST /tracks` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#getting-time-track-info) |
| [List Today Items](actions/list-today-items.md) | `GET /todayItems` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-tasks-and-projects-scheduled-today-including-rolloverauto-schedule-due-items-if-enabled) |
| [List Today Time Blocks](actions/list-today-time-blocks.md) | `GET /todayTimeBlocks` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#get-a-list-of-todays-time-blocks) |
| [Mark Task Done](actions/mark-task-done.md) | `POST /markDone` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#mark-a-task-done) |
| [Set Reminders](actions/set-reminders.md) | `POST /reminder/set` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#set-reminders) |
| [Spend Reward Points](actions/spend-reward-points.md) | `POST /spendRewardPoints` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#spending-reward-points) |
| [Test Credentials](actions/test-credentials.md) | `POST /test` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#test-credentials) |
| [Track Task Time](actions/track-task-time.md) | `POST /track` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#startstop-time-tracking) |
| [Unclaim Reward Points](actions/unclaim-reward-points.md) | `POST /unclaimRewardPoints` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#unclaiming-reward-points) |
| [Update Habit](actions/update-habit.md) | `POST /updateHabit` | [docs](https://github.com/amazingmarvin/MarvinAPI/wiki/Marvin-API#record-a-habit) |
