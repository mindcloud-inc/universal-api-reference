# VoiceGenie Universal API Examples

These examples use the MindCloud API key and VoiceGenie connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Inbound Call Updates

Retrieves inbound call updates from VoiceGenie.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/get-inbound-call-updates?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/get-inbound-call-updates?${params}`, {
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

See the full [Get Inbound Call Updates action reference](actions/get-inbound-call-updates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voiceGenie/latest/actions/get-inbound-call-updates).

## Pause or Resume Campaign

Updates a campaign's running state in VoiceGenie.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/pause-or-resume-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "action": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceGenie/latest/actions/pause-or-resume-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "action": "string"
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
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Pause or Resume Campaign action reference](actions/pause-or-resume-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voiceGenie/latest/actions/pause-or-resume-campaign).
