# Update Form User Security Settings with Global Patron

Updates form user security settings in Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/form/{formId}/usersecurity/{userSecurityId}`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Update Form User Security Settings](https://www.globalpatron.com/developers/api/users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form. |
| `userSecurityId` | path | `string` | yes | ID of the user security record. |
| `has_form_submission` | query | `boolean` | no | Whether the collaborator can view form submissions. |
| `edit_form_submission` | query | `boolean` | no | Whether the collaborator can edit form submissions. |
| `has_report` | query | `boolean` | no | Whether the collaborator can view reports. |
| `edit_form` | query | `boolean` | no | Whether the collaborator can edit the form. |
| `edit_others_form_submission` | query | `boolean` | no | Whether the collaborator can edit other users' submissions. |
