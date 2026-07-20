# Webpushr Universal API Examples

These examples use the MindCloud API key and Webpushr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Subscriber Count



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/get-subscriber-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/get-subscriber-count?${params}`, {
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
      "activeSubscribers": "string",
      "totalLifeTimeSubscribers": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Subscriber Count action reference](actions/get-subscriber-count.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webpushr/latest/actions/get-subscriber-count).

## Send Push to All Subscribers



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/send-push-to-all-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "targetUrl": "https://example.com",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webpushr/latest/actions/send-push-to-all-subscribers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "targetUrl": "https://example.com",
    "title": "string"
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
      "description": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Push to All Subscribers action reference](actions/send-push-to-all-subscribers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/webpushr/latest/actions/send-push-to-all-subscribers).
