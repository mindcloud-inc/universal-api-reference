# Create Form Dropbox Action with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/form/integration/dropbox/actions`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create Form Dropbox Action](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `form` | body | `string` | yes | ID of the form. |
| `actionName` | body | `string` | yes | Name of the Dropbox action. |
| `subFolderName` | body | `string` | yes | Subfolder name. |
| `isCreateSubFolder` | body | `boolean` | yes | Flag to create a subfolder. |
| `folderName` | body | `string` | yes | Name of the Dropbox folder. |
| `sendSubmissionFormat` | body | `string` | yes | Submission format. |
| `selectedFields[]` | body | `array` | yes | Array of form element IDs to include in the upload. |
