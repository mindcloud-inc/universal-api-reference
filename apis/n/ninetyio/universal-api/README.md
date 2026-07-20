# <img src="https://images.mindcloud.co/apps/icons/images-1_1782333770308.png" alt="Ninety.io logo" width="28" height="28"> Ninety.io: Universal API

Access Ninety issues, to-dos, teams, scorecard measurables, rocks, and milestones through the Ninety Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ninetyio/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ninety.io
- **Vendor API docs:** https://api.public.ninety.io/v1/swagger

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Teams](actions/get-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ninetyio/latest/actions/get-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in Ninety.io. |
| [Delete Issue](actions/delete-issue.md) | DELETE | Deletes an existing issue from Ninety.io. |
| [Get Issue by Id](actions/get-issue-by-id.md) | GET | Retrieves an issue from Ninety.io by ID. |
| [Query Issues](actions/query-issues.md) | GET | Retrieves issues from Ninety.io with optional team and interval filters. |
| [Update Issue](actions/update-issue.md) | PUT | Updates an existing issue in Ninety.io. |

### Measurable

| Action | Method | Description |
| --- | --- | --- |
| [Query Measurables](actions/query-measurables.md) | GET | Retrieves measurables from Ninety.io with optional filters. |

### Measurable Note

| Action | Method | Description |
| --- | --- | --- |
| [Delete Measurable Note](actions/delete-measurable-note.md) | DELETE | Deletes a measurable note from Ninety.io for a period. |
| [Create or Update Measurable Note](actions/upsert-measurable-note.md) | PUT | Creates or updates a measurable note in Ninety.io for a period. |

### Measurable Score

| Action | Method | Description |
| --- | --- | --- |
| [Delete Measurable Score](actions/delete-measurable-score.md) | DELETE | Deletes a measurable score from Ninety.io for a period. |
| [Create or Update Measurable Score](actions/upsert-measurable-score.md) | PUT | Creates or updates a measurable score in Ninety.io for a period. |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [Create Milestone](actions/create-milestone.md) | POST | Creates a new milestone in Ninety.io. |
| [Get Milestone by Id](actions/get-milestone-by-id.md) | GET | Retrieves a milestone from Ninety.io by ID. |
| [Update Milestone](actions/update-milestone.md) | PUT | Updates an existing milestone in Ninety.io. |

### Rock

| Action | Method | Description |
| --- | --- | --- |
| [Create Rock](actions/create-rock.md) | POST | Creates a new rock in Ninety.io. |
| [Delete Rock](actions/delete-rock.md) | DELETE | Soft-deletes an existing rock in Ninety.io. |
| [Get Rock by Id](actions/get-rock-by-id.md) | GET | Retrieves a rock from Ninety.io by ID. |
| [Query Rocks](actions/query-rocks.md) | GET | Retrieves rocks from Ninety.io with optional filters. |
| [Update Rock](actions/update-rock.md) | PUT | Updates an existing rock in Ninety.io. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Teams](actions/get-teams.md) | GET | Retrieves teams from Ninety.io. |

### To-do

| Action | Method | Description |
| --- | --- | --- |
| [Create To-Do](actions/create-todo.md) | POST | Creates a new to-do in Ninety.io. |
| [Delete To-Do](actions/delete-todo.md) | DELETE | Deletes an existing to-do from Ninety.io. |
| [Get To-Do by Id](actions/get-todo-by-id.md) | GET | Retrieves a to-do from Ninety.io by ID. |
| [Query To-Dos](actions/query-todos.md) | GET | Retrieves to-dos from Ninety.io with optional filters. |
| [Update To-Do](actions/update-todo.md) | PUT | Updates an existing to-do in Ninety.io. |

