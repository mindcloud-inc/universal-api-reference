# ServiceM8: Create Job Activity



```
POST https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-job-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-job-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/create-job-activity', {
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
| `jobUuid` | string | no | Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `staffUuid` | string | no | Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `startDate` | date | no | Example: `2026-03-01 12:00:00`. |
| `endDate` | date | no | Example: `2026-03-01 13:00:00`. |
| `activityWasScheduled` | boolean | no | Example: `true`. |
| `activityWasRecorded` | boolean | no | Example: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `materialUuid` | string | no | Example: `123e4567-e89b-12d3-a456-426614174000`. |
| `activityWasAutomated` | string | no | Example: `0`. |
| `hasBeenOpened` | boolean | no | Example: `false`. |
| `hasBeenOpenedTimestamp` | date | no | Example: `2026-03-01 12:15:00`. |
| `travelTimeInSeconds` | number | no | Example: `900`. |
| `travelDistanceInMeters` | number | no | Example: `5000`. |
| `uuid` | string | no | Example: `123e4567-e89b-12d3-a456-426614174000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recordUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recordUuid` | string | UUID of the created job activity. |

## Native endpoint

Through the native ServiceM8 API, this operation is `POST /api_1.0/jobactivity.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-activity.md) for the provider-specific parameters and requirements.

