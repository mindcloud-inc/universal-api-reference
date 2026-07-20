# ExpertTexting Universal API Examples

These examples use the MindCloud API key and ExpertTexting connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Balance

Retrieves account balance from ExpertTexting.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/check-balance?${params}`, {
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
      "balance": 1
    }
  ],
  "meta": {}
}
```

See the full [Check Balance action reference](actions/check-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/expertTexting/latest/actions/check-balance).

## Send MMS

Creates an MMS message in ExpertTexting.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/send-mms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": "string",
  "mediaUrls": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expertTexting/latest/actions/send-mms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to": "string",
    "mediaUrls": "https://example.com"
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
      "messageCount": 1,
      "messageId": "string",
      "price": 1
    }
  ],
  "meta": {}
}
```

See the full [Send MMS action reference](actions/send-mms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/expertTexting/latest/actions/send-mms).
