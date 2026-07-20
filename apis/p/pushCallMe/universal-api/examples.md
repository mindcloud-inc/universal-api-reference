# PushCallMe Universal API Examples

These examples use the MindCloud API key and PushCallMe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Call Status

Retrieves call status details from PushCallMe.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/get-call-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/get-call-status?${params}`, {
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
  "data": [
    {
      "availableCalls": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endedAt": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "id": "string",
      "isMissed": true,
      "plan": "string",
      "status": "string",
      "teamId": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Call Status action reference](actions/get-call-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushCallMe/latest/actions/get-call-status).

## Make Phone Call

Creates a new phone call in PushCallMe.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/make-phone-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushCallMe/latest/actions/make-phone-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to": "string"
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
      "from": "string",
      "message": "string",
      "requestId": "string",
      "success": true,
      "to": "string"
    }
  ],
  "meta": {}
}
```

See the full [Make Phone Call action reference](actions/make-phone-call.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pushCallMe/latest/actions/make-phone-call).
