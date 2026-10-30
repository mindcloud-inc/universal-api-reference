# Replace Submission with GoCanvas

## Endpoint

- **Method:** `PUT`
- **Path:** `/submissions/:submissionId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Replace Submission](https://api.gocanvas.com/api/v3/docs#replace-a-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `string` | yes | Numeric ID or mobile GUID of the submission. |
| `submission` | body | `object` | no | Submission identification object; documentation conflicts with URL-only examples. |
| `submission.id` | body | `number` | no | Numeric submission ID; request table marks this required despite URL-only examples. |
| `edit_guid` | body | `string` | no | Reuse the same nonempty GUID on retries of one edit to avoid applying it twice. |
| `finalize` | body | `boolean` | no | True finalizes; false re-saves the draft. GoCanvas defaults to true. |
| `last_sheet_id` | body | `number` | no | Draft resume point, stored when re-saving. |
| `next_assigned_workflow_user_id` | body | `number` | no | User to assign; null or empty unassigns to the pool. |
| `workflow` | body | `object` | no | Workflow handoff to advance, reject, or complete. |
| `workflow.handoff_id` | body | `number` | no | Handoff step; null or -1 completes the workflow. |
| `workflow.handoff_user_id` | body | `number` | no | User to hand off to. |
| `workflow.handoff_email` | body | `string` | no | Email to hand off to, alternative to Handoff User ID. |
| `workflow.handoff_rejected` | body | `boolean` | no | Reject the current handoff when true. |
| `workflow.handoff_rejected_note` | body | `string` | no | Reason for rejection. |
| `responses[]` | body | `array<object>` | yes | Complete response set. All existing responses omitted from this array will be deleted; an explicit empty array deletes all responses. |
| `responses[].value_id` | body | `number` | no | ID of an existing submission value. |
| `responses[].entry_id` | body | `number` | no | Form entry ID for a new response when no value exists. |
| `responses[].value` | body | `string` | no | Text data for the response. |
| `responses[].updated` | body | `boolean` | no | Set false to preserve an unchanged existing value, including its media. A Value ID alone can clear it. Requires Value ID; do not combine with value or delete. |
| `responses[].displayed` | body | `boolean` | no | Whether the value is shown on mobile. |
| `responses[].delete` | body | `boolean` | no | Remove this response when true. |
| `responses[].multi_key` | body | `string` | no | Looped value reference; required for looped forms. |
