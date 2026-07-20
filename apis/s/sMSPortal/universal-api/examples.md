# SMSPortal Universal API Examples

These examples use the MindCloud API key and SMSPortal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Balance



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/retrieve-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/retrieve-balance?${params}`, {
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
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Balance action reference](actions/retrieve-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSPortal/latest/actions/retrieve-balance).

## Send Messages



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/send-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ],
  "messages[].content": "string",
  "messages[].destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/send-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}],
    "messages[].content": "string",
    "messages[].destination": "string"
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
      "sendResponse": {},
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

See the full [Send Messages action reference](actions/send-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sMSPortal/latest/actions/send-messages).
