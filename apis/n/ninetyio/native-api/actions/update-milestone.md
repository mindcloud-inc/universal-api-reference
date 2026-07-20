# Update Milestone with Ninety.io

Updates an existing milestone in Ninety.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/milestones/:id`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Update Milestone](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `title` | body | `string` | no | The title of the Milestone |
| `description` | body | `string` | no | The description of the Milestone |
| `dueDate` | body | `date` | no | The due date of the Milestone |
| `isDone` | body | `boolean` | no | Set to true to mark the Milestone as done |
| `ownedByUserId` | body | `string` | no | The Id of the user who owns this Milestone |
| `completedDate` | body | `date` | no | The date the Milestone was completed |
| `followers[]` | body | `array<string>` | no | Array of user Ids who are following this Milestone |
