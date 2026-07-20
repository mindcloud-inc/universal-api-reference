# CalendarHero: Create Meeting Type

Creates a meeting type in CalendarHero.

```
POST https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/create-meeting-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CalendarHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/create-meeting-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendarHero/latest/actions/create-meeting-type', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CalendarHero API returns.

## Native endpoint

Through the native CalendarHero API, this operation is `POST /user/meeting/{type}` (base URL `https://api.calendarhero.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-meeting-type.md) for the provider-specific parameters and requirements.

