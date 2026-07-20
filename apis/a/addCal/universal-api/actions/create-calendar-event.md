# AddCal: Create Calendar Event

Creates an event in a specific AddCal calendar.

```
POST https://connect.mindcloud.co/v1/universal/addCal/latest/actions/create-calendar-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/addCal/latest/actions/create-calendar-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/addCal/latest/actions/create-calendar-event', {
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AddCal API returns.

## Native endpoint

Through the native AddCal API, this operation is `POST /calendars/:calendar_public_id/events` (base URL `https://addcal.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar-event.md) for the provider-specific parameters and requirements.

