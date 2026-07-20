# TopMessage Universal API Examples

These examples use the MindCloud API key and TopMessage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Messages

Retrieves sent and received messages from TopMessage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/list-messages?${params}`, {
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
      "data": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

See the full [List Messages action reference](actions/list-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/topMessage/latest/actions/list-messages).

## Send Bulk SMS

Creates a bulk SMS message in TopMessage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/send-bulk-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to[]": [
    "string"
  ],
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/send-bulk-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to[]": ["string"],
    "text": "string"
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Send Bulk SMS action reference](actions/send-bulk-sms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/topMessage/latest/actions/send-bulk-sms).
