# Vadootv Universal API Examples

These examples use the MindCloud API key and Vadootv connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get my balance

Retrieves your current credit balance from Vadootv.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-my-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-my-balance?${params}`, {
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

See the full [Get my balance action reference](actions/get-my-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vadootv/latest/actions/get-my-balance).

## Add captions

Creates a captioned video in Vadootv.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/add-captions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/video.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/add-captions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com/video.mp4"
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
      "vid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add captions action reference](actions/add-captions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vadootv/latest/actions/add-captions).
