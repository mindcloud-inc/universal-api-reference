# List Iteration Stories with Shortcut

## Endpoint

- **Method:** `GET`
- **Path:** `/iterations/:iterationPublicId/stories`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [List Iteration Stories](https://developer.shortcut.com/api/rest/v3#List-Iteration-Stories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `iterationPublicId` | path | `number` | yes | The public ID of the iteration. |
| `includes_description` | query | `boolean` | no | Whether to include story descriptions in the response. |
