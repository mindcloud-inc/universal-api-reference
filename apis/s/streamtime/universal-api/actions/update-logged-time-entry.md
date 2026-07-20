# Streamtime: Update Logged Time Entry



```
PUT https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/update-logged-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/update-logged-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "loggedTimeId": "47325447"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/update-logged-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "loggedTimeId": "47325447"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `loggedTimeId` | number | yes | Logged time entry ID. Example: `47325447`. |
| `userId` | number | no | User ID for the logged time entry. Example: `185869`. |
| `date` | string | no | Date for the logged time entry. Example: `2026-03-04`. |
| `minutes` | number | no | Tracked minutes for the logged time entry. Example: `195`. |
| `jobId` | number | no | Job ID linked to the logged time entry. Example: `2079189`. |
| `jobItemUserId` | number | no | Job item user ID linked to the logged time entry. Example: `11452290`. |
| `notes` | string | no | Notes for the logged time entry. Example: `This is a logged To Do. Drag to adjust the time you spent, which is reflected in the job`. |
| `private` | boolean | no | Whether the logged time entry is private. |
| `loggedTimeStatus` | object | no | Logged time status object. |
| `loggedTimeStatus.id` | list<number> | no | Logged Time Status ID (1=Incomplete, 2=Complete, 3=Deleted). One of: `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDatetime": "2026-05-07T12:00:00.000Z",
      "cost": 1,
      "date": "string",
      "id": 1,
      "jobId": 1,
      "jobItemUserId": 1,
      "loggedTimeStatus": {},
      "minutes": 1,
      "notes": "string",
      "private": true,
      "scheduleNotes": "string",
      "totalCostExTax": 1,
      "totalExTax": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedDatetime` | date | Completed timestamp |
| `cost` | number | Logged time cost |
| `date` | string | Logged time date |
| `id` | number | Logged time entry ID |
| `jobId` | number | Job ID linked to the logged time entry |
| `jobItemUserId` | number | Job item user ID linked to the logged time entry |
| `loggedTimeStatus` | object | Logged time status object |
| `minutes` | number | Tracked minutes |
| `notes` | string | Logged time notes |
| `private` | boolean | Whether the logged time entry is private |
| `scheduleNotes` | string | Schedule notes |
| `totalCostExTax` | number | Total cost excluding tax |
| `totalExTax` | number | Total amount excluding tax |
| `userId` | number | User ID for the logged time entry |

## Native endpoint

Through the native Streamtime API, this operation is `PUT /logged_times/:logged_time_id` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-logged-time-entry.md) for the provider-specific parameters and requirements.

