# Update To-Do with Ninety.io

Updates an existing to-do in Ninety.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/todos/:id`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Update To-Do](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The To-Do Id |
| `completed` | body | `boolean` | no | Whether the To-Do is completed |
| `archived` | body | `boolean` | no | Whether the To-Do is archived |
| `dueDate` | body | `date` | no | Due date in ISO format |
| `teamId` | body | `string` | no | The team Id |
| `title` | body | `string` | no | The title of the To-Do |
| `description` | body | `string` | no | The description of the To-Do |
| `repeat` | body | `string` | no | Repeat pattern |
| `userId` | body | `string` | no | User Id to assign the To-Do to |
