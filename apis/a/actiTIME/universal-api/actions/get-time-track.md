# actiTIME: Get Time Track

Retrieves time track records from actiTIME by date range.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-time-track
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-time-track?connectionId=$CONNECTION_ID&dateFrom=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-time-track?${params}`, {
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
| `approved` | boolean | no | Filter approved vs not-approved time track. |
| `customerIds` | string | no | Comma-separated customer ids. |
| `dateFrom` | string | yes | Start date of requested time track in YYYY-MM-DD format. |
| `dateTo` | string | no | End date of requested time track in YYYY-MM-DD format. |
| `includeReferenced` | string | no | Comma-separated referenced objects to include. |
| `projectIds` | string | no | Comma-separated project ids. |
| `stopAfter` | number | no | Approximate number of time-track records to return. |
| `taskIds` | string | no | Comma-separated task ids. |
| `userIds` | string | no | Comma-separated user ids. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "dayOffset": 1,
      "records": [
        {
          "taskId": 1,
          "time": 1
        }
      ],
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Time-track date. |
| `dayOffset` | number | Offset in days from the requested start date. |
| `records[].taskId` | number | Tracked task identifier for the day. |
| `records[].time` | number | Tracked time in minutes for the task. |
| `userId` | number | User identifier. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /timetrack` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-track.md) for the provider-specific parameters and requirements.

