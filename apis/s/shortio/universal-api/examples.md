# Short.io Universal API Examples

These examples use the MindCloud API key and Short.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Domains

Retrieves domains from Short.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/list-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortio/latest/actions/list-domains?${params}`, {
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
      "caseSensitive": true,
      "clientStorage": {},
      "cloaking": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enableAI": true,
      "enableConversionTracking": true,
      "exportEnabled": true,
      "hasFavicon": true,
      "hideReferer": true,
      "hideVisitorIp": true,
      "hostname": "Ava Chen",
      "httpsLevel": "string",
      "httpsLinks": true,
      "id": 1,
      "incrementCounter": "string",
      "integrationAdroll": "string",
      "integrationFB": "string",
      "integrationGA": "string",
      "integrationGTM": "string",
      "isFavorite": true,
      "linkType": "https://example.com",
      "qrScanTracking": true,
      "robots": "string",
      "segmentKey": "string",
      "sslCertExpirationDate": "2026-05-07T12:00:00.000Z",
      "sslCertInstalledSuccess": true,
      "state": "string",
      "teamId": 1,
      "unicodeHostname": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webhookURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Domains action reference](actions/list-domains.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shortio/latest/actions/list-domains).

## Add Single Tag to Links in Bulk

Adds a tag to links in bulk in Short.io.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shortio/latest/actions/add-single-tag-to-links-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tag": "string",
  "linkIds[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortio/latest/actions/add-single-tag-to-links-in-bulk', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tag": "string",
    "linkIds[]": ["https://example.com"]
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Single Tag to Links in Bulk action reference](actions/add-single-tag-to-links-in-bulk.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shortio/latest/actions/add-single-tag-to-links-in-bulk).
