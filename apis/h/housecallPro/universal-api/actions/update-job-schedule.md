# Housecall Pro: Update Job Schedule



```
PUT https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/update-job-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/update-job-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "string",
  "startTime": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/update-job-schedule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "string",
    "startTime": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | string | yes | The ID of the job. |
| `startTime` | date | yes | Start time of the job in ISO-8601 format. |
| `endTime` | date | no | End time of the job in ISO-8601 format. |
| `arrivalWindowInMinutes` | number | no | Arrival window in minutes. |
| `notify` | boolean | no | Notify the customer of the schedule update. |
| `notifyPro` | boolean | no | Notify the employee of the schedule update. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expand[]` | array<string> | no | Additional fields to expand in the response. |
| `dispatchedEmployees[]` | array<object> | no | Dispatched employees payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointments": [
        {}
      ],
      "arrivalWindow": 1,
      "scheduledEnd": "2026-05-07T12:00:00.000Z",
      "scheduledStart": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointments` | array<object> | Appointments returned for the updated schedule. |
| `arrivalWindow` | number | Arrival window in minutes. |
| `scheduledEnd` | date | Scheduled job end time. |
| `scheduledStart` | date | Scheduled job start time. |

## Native endpoint

Through the native Housecall Pro API, this operation is `PUT /jobs/:job_id/schedule` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job-schedule.md) for the provider-specific parameters and requirements.

