# Campaign Cleaner Universal API Examples

These examples use the MindCloud API key and Campaign Cleaner connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves remaining credits from Campaign Cleaner.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-credits?${params}`, {
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
      "credits": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/campaignCleaner/latest/actions/get-credits).

## Send Campaign

Submits a campaign for processing in Campaign Cleaner.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/send-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "send_campaign.campaign_html": "string",
  "send_campaign.campaign_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/send-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "send_campaign.campaign_html": "string",
    "send_campaign.campaign_name": "Ava Chen"
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
      "campaign": {},
      "error": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Campaign action reference](actions/send-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/campaignCleaner/latest/actions/send-campaign).
