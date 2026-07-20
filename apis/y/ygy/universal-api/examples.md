# y.gy Universal API Examples

These examples use the MindCloud API key and y.gy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Links

Retrieves short links from y.gy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ygy/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ygy/latest/actions/list-links?${params}`, {
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
      "Android Link Destination": "https://example.com",
      "Bot Protection": true,
      "Captcha": true,
      "Created At": "string",
      "Destination URL": "https://example.com",
      "Domain": "string",
      "Expiration Date": "string",
      "Has Password": true,
      "ID": 1,
      "iOS Link Destination": "https://example.com",
      "Name": "Ava Chen",
      "OG Description": "string",
      "OG Image": "string",
      "OG Title": "string",
      "Organization ID": 1,
      "QR Code Background Hex": "string",
      "QR Code Foreground Hex": "string",
      "QR Code PNG": "string",
      "QR Code SVG": "string",
      "Suffix": "string",
      "Tags": [
        {}
      ],
      "URL": "https://example.com",
      "Webhook URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Links action reference](actions/list-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ygy/latest/actions/list-links).

## Create Short Link

Creates a new short link in y.gy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ygy/latest/actions/create-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ygy/latest/actions/create-short-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationUrl": "https://example.com"
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
      "Android Link Destination": "https://example.com",
      "Bot Protection": true,
      "Captcha": true,
      "Created At": "string",
      "Destination URL": "https://example.com",
      "Domain": "string",
      "Expiration Date": "string",
      "Has Password": true,
      "ID": 1,
      "iOS Link Destination": "https://example.com",
      "Name": "Ava Chen",
      "OG Description": "string",
      "OG Image": "string",
      "OG Title": "string",
      "Organization ID": 1,
      "QR Code Background Hex": "string",
      "QR Code Foreground Hex": "string",
      "QR Code PNG": "string",
      "QR Code SVG": "string",
      "Suffix": "string",
      "Tags": [
        {}
      ],
      "URL": "https://example.com",
      "Webhook URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Short Link action reference](actions/create-short-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ygy/latest/actions/create-short-link).
