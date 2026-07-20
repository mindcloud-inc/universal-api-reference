# Move Form Item with Google Forms

Moves a form item within Google Forms.

## Endpoint

- **Method:** `POST`
- **Path:** `/:formId:batchUpdate`
- **Base URL:** `https://forms.googleapis.com/v1/forms`
- **Official documentation:** [Move Form Item](https://developers.google.com/workspace/forms/api/reference/rest/v1/forms/batchUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form identifier. |
| `originalIndex` | body | `number` | yes | Current index of the item to move. |
| `newIndex` | body | `number` | yes | Destination index for the item. |
