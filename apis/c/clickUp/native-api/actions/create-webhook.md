# Create Webhook with ClickUp

## Endpoint

- **Method:** `POST`
- **Path:** `team/:team_id/webhook`
- **Base URL:** `https://api.clickup.com/api/v2/`
- **Official documentation:** [Create Webhook](https://developer.clickup.com/reference/createwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint` | body | `string` | yes | — |
| `events` | body | `list<string>` | yes | Accepted values: `*`, `folderCreated`, `folderDeleted`, `folderUpdated`, `goalCreated`, `goalDeleted`, `goalUpdated`, `keyResultCreated`, `keyResultDeleted`, `keyResultUpdated`, `listCreated`, `listDeleted`, `listUpdated`, `spaceCreated`, `spaceDeleted`, `spaceUpdated`, `taskAssigneeUpdated`, `taskCommentPosted`, `taskCommentUpdated`, `taskCreated`, `taskDeleted`, `taskDueDateUpdated`, `taskMoved`, `taskPriorityUpdated`, `taskStatusUpdated`, `taskTagUpdated`, `taskTimeEstimateUpdated`, `taskTimeTrackedUpdated`, `taskUpdated`. Send multiple values as a array. |
| `folder_id` | body | `number` | no | — |
| `list_id` | body | `number` | no | — |
| `space_id` | body | `number` | no | — |
| `task_id` | body | `string` | no | — |
| `team_id` | path | `list` | yes | — |
