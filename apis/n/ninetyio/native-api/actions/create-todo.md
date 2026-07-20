# Create To-Do with Ninety.io

Creates a new to-do in Ninety.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/todos`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Create To-Do](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | — |
| `description` | body | `string` | no | The description of the To-Do |
| `dueDate` | body | `date` | no | Due date in YYYY-MM-DD format |
| `teamId` | body | `string` | no | The Id of the team to assign this To-Do to |
| `repeat` | body | `string` | no | Recurrence pattern for the To-Do |
| `userId` | body | `string` | no | Id of the user to assign the To-Do to |
