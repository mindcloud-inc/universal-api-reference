# Botmother Universal API Examples

These examples use the MindCloud API key and Botmother connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Trigger External Event For Botmother Users

Triggers an external event in Botmother for users by bm_id.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botmother/latest/actions/trigger-external-event-for-botmother-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "usersBm[]": [
    "string"
  ],
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botmother/latest/actions/trigger-external-event-for-botmother-users', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "usersBm[]": ["string"],
    "data": {}
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
      "limits": {
        "exceeded": true,
        "queued": {
          "big": 1,
          "small": 1
        },
        "remained": {
          "big": 1,
          "small": 1
        }
      },
      "payload": [
        [
          {}
        ]
      ],
      "result": true
    }
  ],
  "meta": {}
}
```

See the full [Trigger External Event For Botmother Users action reference](actions/trigger-external-event-for-botmother-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botmother/latest/actions/trigger-external-event-for-botmother-users).
