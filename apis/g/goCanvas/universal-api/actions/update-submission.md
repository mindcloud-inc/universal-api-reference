# GoCanvas: Update Submission



```
PUT https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "submissionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/update-submission', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "submissionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `submissionId` | string | yes | Numeric ID or mobile GUID of the submission. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `submission` | object | no | Submission identification object; documentation conflicts with URL-only examples. |
| `submission.id` | number | no | Numeric submission ID; request table marks this required despite URL-only examples. |
| `editGuid` | string | no | Reuse the same nonempty GUID on retries of one edit to avoid applying it twice. |
| `finalize` | boolean | no | True finalizes; false re-saves the draft. GoCanvas defaults to true. |
| `lastSheetId` | number | no | Draft resume point, stored when re-saving. |
| `nextAssignedWorkflowUserId` | number | no | User to assign. An invalid, disabled, or unassignable user can clear the current assignee even when GoCanvas returns 200. |
| `workflow` | object | no | Workflow handoff to advance, reject, or complete. |
| `workflow.handoffId` | number | no | Handoff step; null or -1 completes the workflow. |
| `workflow.handoffUserId` | number | no | User to hand off to. |
| `workflow.handoffEmail` | string | no | Email to hand off to, alternative to Handoff User ID. |
| `workflow.handoffRejected` | boolean | no | Reject the current handoff when true. |
| `workflow.handoffRejectedNote` | string | no | Reason for rejection. |
| `responses[]` | array<object> | no | Text responses to update. |
| `responses[].valueId` | number | no | ID of an existing submission value. |
| `responses[].entryId` | number | no | Form entry ID for a new response when no value exists. |
| `responses[].value` | string | no | Text data for the response. |
| `responses[].updated` | boolean | no | Set false to preserve an unchanged existing value, including its media. Without it, resending media without its content GUID can clear the file. Requires Value ID; do not combine with value or delete. |
| `responses[].displayed` | boolean | no | Whether the value is shown on mobile. |
| `responses[].delete` | boolean | no | Remove this response when true. |
| `responses[].multiKey` | string | no | Looped value reference; required for looped forms. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `PATCH /submissions/:submissionId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-submission.md) for the provider-specific parameters and requirements.

