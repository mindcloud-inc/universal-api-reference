# VoiceShot Universal API Examples

These examples use the MindCloud API key and VoiceShot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Configuration

Retrieves a configuration test result from VoiceShot.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/test-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/test-configuration?${params}`, {
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
      "comment": "string",
      "errorId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Configuration action reference](actions/test-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voiceShot/latest/actions/test-configuration).

## Pause Pending Calls

Pauses pending calls in a VoiceShot campaign.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/pause-pending-calls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "menuId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/pause-pending-calls', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "menuId": "string"
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
      "comment": "string",
      "errorId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Pause Pending Calls action reference](actions/pause-pending-calls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voiceShot/latest/actions/pause-pending-calls).
