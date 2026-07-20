# Create Project with Filestage

Creates a new project in Filestage.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Create Project](https://developers.filestage.io/docs/api/3ifqfpvkrrtct-create-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | body | `string` | yes | — |
| `projectTemplateId` | body | `string` | no | — |
| `name` | body | `string` | yes | — |
| `emails[]` | body | `array<string>` | no | This is an array of collaborators' emails. |
| `notifyEmail` | body | `boolean` | no | — |
| `message` | body | `string` | no | — |
