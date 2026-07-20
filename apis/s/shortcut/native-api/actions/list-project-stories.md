# List Project Stories with Shortcut

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectPublicId/stories`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [List Project Stories](https://developer.shortcut.com/api/rest/v3#List-Stories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectPublicId` | path | `number` | yes | The public ID of the project. |
| `includes_description` | query | `boolean` | no | Whether to include story descriptions in the response. |
