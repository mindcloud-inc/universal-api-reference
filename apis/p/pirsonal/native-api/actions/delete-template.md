# Delete Template with Pirsonal

Deletes an existing template from Pirsonal.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `https://app.pirsonal.com`
- **Official documentation:** [Delete Template](https://app.pirsonal.com/docAPI#Template_Delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateID` | body | `string` | yes | ID of the template to delete. |
| `removeExternalFiles` | body | `boolean` | yes | Whether Pirsonal should remove external videos too, such as YouTube files. |
