# ActivitySmith Universal API Examples

These examples use the MindCloud API key and ActivitySmith connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## End Live Activity

Ends an existing Live Activity in ActivitySmith.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/end-live-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activitySmith/latest/actions/end-live-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [End Live Activity action reference](actions/end-live-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/activitySmith/latest/actions/end-live-activity).
