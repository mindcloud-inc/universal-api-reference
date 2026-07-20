# SMS8.io Universal API Examples

These examples use the MindCloud API key and SMS8.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Message Status



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/get-message-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/get-message-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

See the full [Get Message Status action reference](actions/get-message-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMS8io/latest/actions/get-message-status).

## Send SMS



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "string",
  "message": "string",
  "devices": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "string",
    "message": "string",
    "devices": "string"
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

See the full [Send SMS action reference](actions/send-sms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMS8io/latest/actions/send-sms).
