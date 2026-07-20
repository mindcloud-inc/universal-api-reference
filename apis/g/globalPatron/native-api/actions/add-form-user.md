# Add Form User with Global Patron

Adds a form user in Global Patron.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/restricted/form/{formId}/usersecurity`
- **Base URL:** `https://api.globalpatron.com`
- **Official documentation:** [Add Form User](https://www.globalpatron.com/developers/api/users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | ID of the form. |
| `collaborator_email` | query | `string` | yes | Email address of the collaborator to add. |
| `has_form_submission` | query | `boolean` | no | Whether the collaborator can view form submissions. |
| `edit_form_submission` | query | `boolean` | no | Whether the collaborator can edit form submissions. |
| `has_report` | query | `boolean` | no | Whether the collaborator can view reports. |
| `edit_form` | query | `boolean` | no | Whether the collaborator can edit the form. |
| `edit_others_form_submission` | query | `boolean` | no | Whether the collaborator can edit other users' submissions. |
