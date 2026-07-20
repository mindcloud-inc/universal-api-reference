# Import Project Content with Localazy

Imports localization files into a Localazy project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/import`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Import Project Content](https://localazy.com/docs/api/import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project id or slug. |
| `importAsNew` | body | `boolean` | no | Send imported translations to the review flow instead of making them current immediately. |
| `forceCurrent` | body | `boolean` | no | Overwrite existing current translations. |
| `filterSource` | body | `boolean` | no | Skip importing translations that match the source language text. |
| `forceSource` | body | `boolean` | no | Overwrite the source language values in Localazy. |
| `files[]` | body | `array<object>` | yes | Files and localization content to import. |
| `files[].name` | body | `string` | yes | Filename shown in Localazy. |
| `files[].content` | body | `object` | yes | File content payload including type and language maps. |
