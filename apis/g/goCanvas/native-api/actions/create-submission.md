# Create Submission with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create Submission](https://api.gocanvas.com/api/v3/docs#create-a-basic-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `guid` | body | `string` | yes | Unique GUID to prevent duplicate submissions. |
| `department_id` | body | `number` | no | Department for the submission; required when departments are enabled. |
| `form` | body | `object` | yes | Form to which the submission is made. |
| `form.id` | body | `number` | no | Form ID; provide this or Form GUID. |
| `form.guid` | body | `string` | no | Form GUID; provide this or Form ID. |
| `form.version` | body | `number` | no | Form version; recommended when using a form GUID. |
| `responses[]` | body | `array<object>` | no | Text responses to form entries. |
| `responses[].entry_id` | body | `number` | no | Identifier of the form entry. |
| `responses[].entry_guid` | body | `string` | no | GUID of the form entry, an alternative to entry ID. |
| `responses[].displayed` | body | `boolean` | no | Whether the entry is displayed for user entry or calculated. |
| `responses[].value` | body | `string` | no | Text response data for the entry. |
| `responses[].multi_key` | body | `string` | no | Looped value reference; required for looped forms. |
| `finalize` | body | `boolean` | no | True finalizes; false saves a cloud draft. GoCanvas defaults to true. |
| `last_sheet_id` | body | `number` | no | Resume point of a draft. |
| `recipients[]` | body | `array<string>` | no | Email addresses to receive a copy of the submission. |
| `next_assigned_workflow_user_id` | body | `number` | no | Assign to a user; a blank value places the submission in the claimable pool. |
| `workflow` | body | `object` | no | Workflow handoff to advance. |
| `workflow.workflow_id` | body | `number` | no | Identifier of the workflow. |
| `workflow.handoff_id` | body | `number` | no | Handoff step; null or -1 completes the workflow. |
| `workflow.handoff_user_id` | body | `number` | no | User to hand off to. |
| `workflow.handoff_email` | body | `string` | no | Email to hand off to, alternative to Handoff User ID. |
