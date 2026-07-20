# InflatableOffice: Create Task

Creates a new task in InflatableOffice.

```
POST https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `task_assignedid` | string | no |  |
| `task_assignedto` | string | no |  |
| `task_badge` | string | no |  |
| `task_calendar` | string | no |  |
| `task_desc` | string | no |  |
| `task_email` | string | no |  |
| `task_flag` | string | no |  |
| `task_linkid` | string | no |  |
| `task_linkto` | string | no |  |
| `task_linktype` | string | no |  |
| `task_read` | string | no |  |
| `task_recurring` | string | no |  |
| `task_reminddate` | string | no |  |
| `task_status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "requestTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created task ID. |
| `requestTime` | number | Provider request timestamp. |

## Native endpoint

Through the native InflatableOffice API, this operation is `POST /tasks` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

