# Update Rock with Ninety.io

Updates an existing rock in Ninety.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/rocks/:id`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Update Rock](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `userId` | body | `string` | no | The Id of the user who owns the Rock |
| `teamId` | body | `string` | no | The Id of the team the Rock belongs to |
| `title` | body | `string` | no | The title of the Rock |
| `description` | body | `string` | no | The description of the Rock |
| `statusCode` | body | `string` | no | The status of the Rock |
| `levelCode` | body | `string` | no | The level of the Rock |
| `quarter` | body | `string` | no | The quarter associated with the Rock |
| `dueDate` | body | `date` | no | The due date of the Rock |
| `rockQuarterYearDueDate` | body | `date` | no | The quarter-aligned year due date of the Rock |
| `archived` | body | `boolean` | no | Set to true to archive the Rock, false to unarchive it |
| `futureScope` | body | `string` | no | The future scope of the Rock |
| `additionalTeamIds[]` | body | `array<string>` | no | Array of additional team Ids that can also view this Rock |
