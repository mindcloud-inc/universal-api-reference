# List Epic Stories with Shortcut

## Endpoint

- **Method:** `GET`
- **Path:** `/epics/:epicPublicId/stories`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [List Epic Stories](https://developer.shortcut.com/api/rest/v3#List-Epic-Stories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `epicPublicId` | path | `number` | yes | The public ID of the epic. |
| `includes_description` | query | `boolean` | no | Whether to include story descriptions in the response. |
