# Create Milestone with Ninety.io

Creates a new milestone in Ninety.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/milestones`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Create Milestone](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rockId` | body | `string` | yes | — |
| `title` | body | `string` | yes | — |
| `dueDate` | body | `date` | yes | — |
| `teamId` | body | `string` | yes | — |
| `description` | body | `string` | no | The description of the Milestone |
| `userOrdinal` | body | `number` | no | The ordinal position of this Milestone for the user |
| `toDoId` | body | `string` | no | The Id of a related To-Do item, if any |
| `isDone` | body | `boolean` | no | True if the Milestone is already done at creation time |
| `completedDate` | body | `date` | no | The date the Milestone was completed |
