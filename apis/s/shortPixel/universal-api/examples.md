# ShortPixel Universal API Examples

These examples use the MindCloud API key and ShortPixel connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Remote Optimization Status

Retrieves remote image optimization status from ShortPixel.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/check-remote-optimization-status?connectionId=$CONNECTION_ID&optimizationUrls%5B%5D=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "optimizationUrls[]": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/check-remote-optimization-status?${params}`, {
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
      "AVIFLosslessSize": "string",
      "AVIFLosslessURL": "https://example.com",
      "AVIFLossySize": "string",
      "AVIFLossyURL": "https://example.com",
      "LoselessSize": 1,
      "LosslessSize": 1,
      "LosslessURL": "https://example.com",
      "LossySize": 1,
      "LossyURL": "https://example.com",
      "OriginalSize": 1,
      "OriginalURL": "https://example.com",
      "PercentImprovement": "string",
      "Status": {},
      "TimeStamp": "string",
      "Unlimited": true,
      "WebPLoselessSize": "string",
      "WebPLosslessSize": "string",
      "WebPLosslessURL": "https://example.com",
      "WebPLossySize": "string",
      "WebPLossyURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Check Remote Optimization Status action reference](actions/check-remote-optimization-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shortPixel/latest/actions/check-remote-optimization-status).

## Optimize Remote Image Direct

Creates an optimized image directly from a remote URL in ShortPixel.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-remote-image-direct" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-remote-image-direct', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com"
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Optimize Remote Image Direct action reference](actions/optimize-remote-image-direct.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shortPixel/latest/actions/optimize-remote-image-direct).
