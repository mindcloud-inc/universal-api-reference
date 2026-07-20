# Update Form OneDrive Action with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form/integration/one-drive/actions/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form OneDrive Action](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the OneDrive action to update. |
| `actionName` | body | `string` | yes | Updated name of the OneDrive action. |
| `subFolderName` | body | `string` | yes | Updated subfolder name. |
| `isCreateSubFolder` | body | `boolean` | yes | Updated flag to create a subfolder. |
| `sendSubmissionFormat` | body | `string` | yes | Updated submission format. |
| `selectedFields[]` | body | `array` | yes | Updated array of form element IDs to include in the upload. |
| `isDisabled` | body | `boolean` | yes | Flag to disable the action. |
