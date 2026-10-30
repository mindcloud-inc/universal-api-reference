# GoCanvas: Create Dispatch



```
POST https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-dispatch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-dispatch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": 1,
  "dispatchType": "immediate_dispatch"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-dispatch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": 1,
    "dispatchType": "immediate_dispatch"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | number | yes | The identifier of the form. |
| `dispatchType` | list | yes | Choose an immediate, scheduled, or recurring dispatch. One of: `immediate_dispatch`, `recurring_dispatch`, `scheduled_dispatch`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assigneeId` | number | no | User assigned to the dispatch; omit to leave it unassigned. |
| `name` | string | no | Short name displayed on the Dispatch Calendar and calendar invitation. |
| `description` | string | no | Short description displayed on the assignee's mobile device. |
| `departmentId` | number | no | Department for the dispatch; if omitted, GoCanvas uses the assignee's default department or the form's originating department. |
| `customerId` | number | no | Customer to associate with the dispatch. |
| `projectId` | number | no | Project to associate with the dispatch. |
| `siteId` | number | no | Site to associate with the dispatch. |
| `responses[]` | array<object> | no | Form entry responses used to pre-populate the submission. |
| `responses[].entryId` | number | no | Identifier of the form entry; entry GUID is an alternative in the immediate-dispatch documentation. |
| `responses[].entryGuid` | string | no | Entry GUID, an alternative to entry ID documented for immediate dispatches. |
| `responses[].value` | string | no | Response data for the entry. |
| `responses[].multiKey` | string | no | Looped value reference; required for looped forms. |
| `scheduledAt` | string | no | Required for scheduled and recurring dispatches; example: 12/1/2024 8:00:00 AM. |
| `scheduledEnd` | string | no | Required for scheduled and recurring dispatches; example: 12/1/2024 12:00:00 PM. |
| `reminderInterval` | number | no | Minutes before the dispatch event to send a reminder. Scheduled-dispatch documentation lists this as optional and also as required. |
| `sendCalendarInvite` | boolean | no | Send a calendar invitation when true. |
| `sendNotification` | boolean | no | Send a mobile push notification when true; documented for immediate dispatches. |
| `noFormAssignment` | boolean | no | Allow creation without the assignee being assigned to the form when true. |
| `repeatInterval` | list | no | Required for recurring dispatches. One of: `daily`, `monthly_date`, `monthly_day`, `weekdays`, `weekly`, `yearly`. |
| `repeatEndsOption` | list | no | Required for recurring dispatches. One of: `ends_after`, `ends_on`. |
| `repeatEndsOn` | string | no | Required when repeat ends option is ends_on; format MM/DD/YYYY. |
| `repeatOccurrences` | number | no | Required when repeat ends option is ends_after. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `POST /dispatches` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dispatch.md) for the provider-specific parameters and requirements.

