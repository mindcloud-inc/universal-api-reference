# GoCanvas: Create Submission



```
POST https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-submission" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guid": "string",
  "form": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-submission', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guid": "string",
    "form": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guid` | string | yes | Unique GUID to prevent duplicate submissions. |
| `form` | object | yes | Form to which the submission is made. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `departmentId` | number | no | Department for the submission; required when departments are enabled. |
| `form.id` | number | no | Form ID; provide this or Form GUID. |
| `form.guid` | string | no | Form GUID; provide this or Form ID. |
| `form.version` | number | no | Form version; recommended when using a form GUID. |
| `responses[]` | array<object> | no | Text responses to form entries. |
| `responses[].entryId` | number | no | Identifier of the form entry. |
| `responses[].entryGuid` | string | no | GUID of the form entry, an alternative to entry ID. |
| `responses[].displayed` | boolean | no | Whether the entry is displayed for user entry or calculated. |
| `responses[].value` | string | no | Text response data for the entry. |
| `responses[].multiKey` | string | no | Looped value reference; required for looped forms. |
| `finalize` | boolean | no | True finalizes; false saves a cloud draft. GoCanvas defaults to true. |
| `lastSheetId` | number | no | Resume point of a draft. |
| `recipients[]` | array<string> | no | Email addresses to receive a copy of the submission. |
| `nextAssignedWorkflowUserId` | number | no | Assign to a user; a blank value places the submission in the claimable pool. |
| `workflow` | object | no | Workflow handoff to advance. |
| `workflow.workflowId` | number | no | Identifier of the workflow. |
| `workflow.handoffId` | number | no | Handoff step; null or -1 completes the workflow. |
| `workflow.handoffUserId` | number | no | User to hand off to. |
| `workflow.handoffEmail` | string | no | Email to hand off to, alternative to Handoff User ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `POST /submissions` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-submission.md) for the provider-specific parameters and requirements.

