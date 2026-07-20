# HTML/CSS to Image app Universal API Examples

These examples use the MindCloud API key and HTML/CSS to Image app connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/get-usage?${params}`, {
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
      "data": {
        "day": {
          "value20260313T000000Z": 1
        },
        "hour": {
          "value20260313T150000Z": 1,
          "value20260313T160000Z": 1
        },
        "month": {
          "value20260301T000000Z": 1
        }
      },
      "perBillingPeriod": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hTMLCSSToImageApp/latest/actions/get-usage).

## Create Image



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/create-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Image action reference](actions/create-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hTMLCSSToImageApp/latest/actions/create-image).
