# Create Schedule with Morningmate

Creates a schedule in a Morningmate project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/posts/projects/[:projectId]/schedules`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Create Schedule](https://api.morningmate.com/docs/api/v1/posts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `registerId` | body | `string` | yes |
| `title` | body | `string` | yes |
| `isAllDay` | body | `boolean` | yes |
| `startDateTime` | body | `string` | yes |
| `endDateTime` | body | `string` | yes |
