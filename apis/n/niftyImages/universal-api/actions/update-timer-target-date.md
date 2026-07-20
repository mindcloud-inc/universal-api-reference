# NiftyImages: Update Timer Target Date

Updates a timer target date in NiftyImages.

```
PUT https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/update-timer-target-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/update-timer-target-date" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "TimerImageUrl": "https://example.com",
  "TargetDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/update-timer-target-date', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "TimerImageUrl": "https://example.com",
    "TargetDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `TimerImageUrl` | string | yes | URL of the timer image to update. |
| `TargetDate` | string | yes | New timer target date in ISO 8601 format. |
| `Format` | string | no | Date format when TargetDate is not already ISO 8601. |
| `IsUtc` | boolean | no | Set to true to adjust the target date using the timer timezone. |
| `AddHours` | number | no | Hours to add to the target date. |
| `AddDays` | number | no | Days to add to the target date. |
| `AddMonths` | number | no | Months to add to the target date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "TimerImageUrl": "https://example.com",
      "TimerTimezone": "string",
      "UpdatedTargetTimezone": "2026-05-07T12:00:00.000Z",
      "UpdatedTargetUtc": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `TimerImageUrl` | string |  |
| `TimerTimezone` | string |  |
| `UpdatedTargetTimezone` | date |  |
| `UpdatedTargetUtc` | date |  |

## Native endpoint

Through the native NiftyImages API, this operation is `PUT /Timer/Update` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-timer-target-date.md) for the provider-specific parameters and requirements.

