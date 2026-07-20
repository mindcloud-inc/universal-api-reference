# Linkly Universal API Examples

These examples use the MindCloud API key and Linkly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Links

Retrieves links from Linkly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkly/latest/actions/list-links?${params}`, {
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
      "links": [
        {}
      ],
      "pageNumber": 1,
      "pageSize": 1,
      "totalEntries": 1,
      "totalPages": 1,
      "totalRows": 1,
      "workspaceLinkCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Links action reference](actions/list-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkly/latest/actions/list-links).

## Create Link

Creates a new link in Linkly.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkly/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkly/latest/actions/create-link', {
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
      "blockBots": true,
      "bodyTags": "string",
      "cloaking": true,
      "deleted": true,
      "domain": "string",
      "enabled": true,
      "expiryClicks": 1,
      "expiryDatetime": "string",
      "expiryDestination": "string",
      "fbPixelId": "string",
      "forwardParams": true,
      "fullUrl": "https://example.com",
      "ga4TagId": "string",
      "gtmId": "string",
      "headTags": "string",
      "hideReferrer": true,
      "id": 1,
      "insertedAt": "string",
      "linkifyWords": "https://example.com",
      "name": "Ava Chen",
      "note": "string",
      "ogDescription": "string",
      "ogImage": "string",
      "ogTitle": "string",
      "publicAnalytics": true,
      "replacements": "string",
      "rules": [
        {}
      ],
      "skipSocialCrawlerTracking": true,
      "slug": "string",
      "spam": true,
      "url": "https://example.com",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmSource": "string",
      "utmTerm": "string",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Link action reference](actions/create-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkly/latest/actions/create-link).
