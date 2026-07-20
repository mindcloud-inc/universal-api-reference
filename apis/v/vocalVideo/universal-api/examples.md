# Vocal Video Universal API Examples

These examples use the MindCloud API key and Vocal Video connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from Vocal Video.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/get-account?${params}`, {
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
      "account": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vocalVideo/latest/actions/get-account).

## Subscribe to Replies

Creates a reply webhook subscription in Vocal Video.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/subscribe-to-replies" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "zapUrl": "https://example.com/webhooks/vocal-video/replies"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vocalVideo/latest/actions/subscribe-to-replies', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "zapUrl": "https://example.com/webhooks/vocal-video/replies"
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Subscribe to Replies action reference](actions/subscribe-to-replies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vocalVideo/latest/actions/subscribe-to-replies).
