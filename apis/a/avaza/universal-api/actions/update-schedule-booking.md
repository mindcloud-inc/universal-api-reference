# Avaza: Update Schedule Booking

Updates an existing schedule booking in Avaza.

```
PUT https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-schedule-booking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-schedule-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/update-schedule-booking', {
  method: 'PUT',
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
| `scheduleseriesid` | number | no |  |
| `useridfk` | number | no |  |
| `hoursperday` | number | no |  |
| `totalduration` | number | no |  |
| `durationtype` | string | no | Possible values are "HoursPerDay" or "TotalDuration" |
| `scheduleondaysoff` | boolean | no |  |
| `projectidfk` | number | no |  |
| `categoryidfk` | number | no |  |
| `taskidfk` | number | no |  |
| `notes` | string | no |  |
| `startdate` | date | no |  |
| `enddate` | date | no |  |
| `starttime` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `PUT /ScheduleSeries/EditBooking` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-schedule-booking.md) for the provider-specific parameters and requirements.

