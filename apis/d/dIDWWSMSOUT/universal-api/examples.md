# DIDWW SMS OUT Universal API Examples

These examples use the MindCloud API key and DIDWW SMS OUT connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Send Bulk SMS With Campaign

Creates bulk outbound SMS messages in DIDWW SMS OUT with a campaign ID.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dIDWWSMSOUT/latest/actions/send-bulk-sms-with-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinations": "string",
  "content": "string",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dIDWWSMSOUT/latest/actions/send-bulk-sms-with-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinations": "string",
    "content": "string",
    "campaignId": "string"
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
      "data": {
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Send Bulk SMS With Campaign action reference](actions/send-bulk-sms-with-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dIDWWSMSOUT/latest/actions/send-bulk-sms-with-campaign).
