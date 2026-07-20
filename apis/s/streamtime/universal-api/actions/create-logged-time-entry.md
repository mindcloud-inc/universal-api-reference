# Streamtime: Create Logged Time Entry



```
POST https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-logged-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-logged-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "789",
  "date": "2026-03-04",
  "minutes": "90",
  "loggedTimeStatus.id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-logged-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "789",
    "date": "2026-03-04",
    "minutes": "90",
    "loggedTimeStatus.id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | User ID for the logged time entry. Example: `789`. |
| `date` | string | yes | Date for the logged time entry. Example: `2026-03-04`. |
| `minutes` | number | yes | Tracked minutes for the logged time entry. Example: `90`. |
| `jobId` | number | no | Job ID linked to the logged time entry. Example: `2079189`. |
| `jobItemUserId` | number | no | Job item user ID linked to the logged time entry. Example: `11452290`. |
| `notes` | string | no | Notes for the logged time entry. Example: `Reviewed safety procedures`. |
| `private` | boolean | no | Whether the logged time entry is private. |
| `loggedTimeStatus` | object | no | Logged time status object. |
| `loggedTimeStatus.id` | list<number> | yes | Logged Time Status ID (1=Incomplete, 2=Complete, 3=Deleted). One of: `1`, `2`, `3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDatetime": "string",
      "date": "string",
      "id": 1,
      "jobId": 1,
      "jobItemUserId": 1,
      "loggedTimeStatus": {},
      "minutes": 1,
      "notes": "string",
      "private": true,
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
| `completedDatetime` | string | Completion timestamp |
| `date` | string | Logged date |
| `id` | number | Logged time ID |
| `jobId` | number | Related job ID |
| `jobItemUserId` | number | Related job item user ID |
| `loggedTimeStatus` | object | Logged time status |
| `minutes` | number | Logged minutes |
| `notes` | string | Entry notes |
| `private` | boolean | Whether the entry is private |
| `totalExTax` | number | Total excluding tax |
| `userId` | number | User ID |

## Native endpoint

Through the native Streamtime API, this operation is `POST /logged_times` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-logged-time-entry.md) for the provider-specific parameters and requirements.

