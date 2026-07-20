# Update Form Dropbox Action with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form/integration/dropbox/actions/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form Dropbox Action](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the Dropbox action to update. |
| `actionName` | body | `string` | yes | Updated name of the Dropbox action. |
| `subFolderName` | body | `string` | yes | Updated subfolder name. |
| `isCreateSubFolder` | body | `boolean` | yes | Updated flag to create a subfolder. |
| `sendSubmissionFormat` | body | `string` | yes | Updated submission format. |
| `selectedFields[]` | body | `array` | yes | Updated array of form element IDs to include in the upload. |
| `isDisabled` | body | `boolean` | yes | Flag to disable the action. |
