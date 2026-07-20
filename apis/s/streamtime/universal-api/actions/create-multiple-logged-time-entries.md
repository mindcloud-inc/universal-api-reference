# Streamtime: Create Multiple Logged Time Entries



```
POST https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-multiple-logged-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-multiple-logged-time-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "loggedTimes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-multiple-logged-time-entries', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "loggedTimes[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `loggedTimes[]` | array<object> | yes | Array of logged time entry payloads. |

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

Through the native Streamtime API, this operation is `POST /logged_times/bulk` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multiple-logged-time-entries.md) for the provider-specific parameters and requirements.

