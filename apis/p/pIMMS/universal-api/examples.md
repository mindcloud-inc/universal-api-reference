# PIMMS Universal API Examples

These examples use the MindCloud API key and PIMMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve QR Code

Retrieves a QR code image from PIMMS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/retrieve-qr-code?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/retrieve-qr-code?${params}`, {
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
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve QR Code action reference](actions/retrieve-qr-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pIMMS/latest/actions/retrieve-qr-code).

## Create Link

Creates a new deep link in PIMMS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/create-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
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
      "android": "string",
      "archived": true,
      "clicks": 1,
      "comments": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domain": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "image": "string",
      "ios": "string",
      "key": "string",
      "lastClicked": "string",
      "leads": 1,
      "qrCode": "string",
      "shortLink": "https://example.com",
      "tags": [
        {}
      ],
      "title": "string",
      "trackConversion": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": "string",
      "utm_campaign": "string",
      "utm_content": "string",
      "utm_medium": "string",
      "utm_source": "string",
      "utm_term": "string",
      "video": "string",
      "webhookIds": [
        "string"
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Link action reference](actions/create-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pIMMS/latest/actions/create-link).
