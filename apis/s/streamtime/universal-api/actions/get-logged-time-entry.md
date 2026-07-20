# Streamtime: Get Logged Time Entry



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-logged-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-logged-time-entry?connectionId=$CONNECTION_ID&loggedTimeId=47325447" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "loggedTimeId": "47325447"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-logged-time-entry?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `loggedTimeId` | number | yes | Logged time entry ID. Example: `47325447`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDatetime": "2026-05-07T12:00:00.000Z",
      "cost": 1,
      "date": "2026-05-07T12:00:00.000Z",
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
| `date` | date | Logged time date |
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

Through the native Streamtime API, this operation is `GET /logged_times/:logged_time_id` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-logged-time-entry.md) for the provider-specific parameters and requirements.

