# Cronfree Time Scheduler Universal API Examples

These examples use the MindCloud API key and Cronfree Time Scheduler connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Create Schedule

Creates a new schedule in Cronfree Time Scheduler.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cronfreeTimeScheduler/latest/actions/create-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hookUrl": "https://example.com",
  "wdays[]": [
    "string"
  ],
  "months[]": [
    "string"
  ],
  "mdays[]": [
    "string"
  ],
  "hours[]": [
    "string"
  ],
  "minutes[]": [
    "string"
  ],
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cronfreeTimeScheduler/latest/actions/create-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hookUrl": "https://example.com",
    "wdays[]": ["string"],
    "months[]": ["string"],
    "mdays[]": ["string"],
    "hours[]": ["string"],
    "minutes[]": ["string"],
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Schedule action reference](actions/create-schedule.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cronfreeTimeScheduler/latest/actions/create-schedule).
