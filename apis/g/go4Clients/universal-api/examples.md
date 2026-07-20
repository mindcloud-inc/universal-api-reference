# Go4Clients Universal API Examples

These examples use the MindCloud API key and Go4Clients connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves plan and wallet balances from Go4Clients.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/get-balance?${params}`, {
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
      "balance": 1,
      "namePlan": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/go4Clients/latest/actions/get-balance).

## Add Calls to Voice Campaign

Adds calls to an existing Go4Clients voice campaign.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-calls-to-voice-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "voiceCampaignId": "69dd2799f931660008cdc96f",
  "destinationsList[]": "573004445566"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/add-calls-to-voice-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "voiceCampaignId": "69dd2799f931660008cdc96f",
    "destinationsList[]": "573004445566"
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
      "campaignId": "string",
      "campaignName": "Ava Chen",
      "destinationsList": [
        "string"
      ],
      "generatedIds": {},
      "ivrId": "string",
      "priority": "string",
      "recordCall": true,
      "sender": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Calls to Voice Campaign action reference](actions/add-calls-to-voice-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/go4Clients/latest/actions/add-calls-to-voice-campaign).
