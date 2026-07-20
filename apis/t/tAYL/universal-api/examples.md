# TAYL Universal API Examples

These examples use the MindCloud API key and TAYL connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tales



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/list-tales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/list-tales?${params}`, {
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
      "author": "string",
      "byline_author": true,
      "byline_date": true,
      "clearbitLogo": "string",
      "createdAt": {},
      "credits": 1,
      "description": "string",
      "detectedLanguage": "string",
      "excerpt": "string",
      "favIcon": "string",
      "id": "string",
      "language": "string",
      "metaLanguage": "string",
      "publishedAt": "string",
      "publisher": "string",
      "shareImage": "string",
      "source": "string",
      "status": "string",
      "storageMetadataAudio": {},
      "storageMetadataHtml": {},
      "storageMetadataSsml": {},
      "stripeSubscriptionUsageItemId": "string",
      "stripeUsageRecordId": "string",
      "submittedUrl": "https://example.com",
      "summaryLength": 1,
      "title": "string",
      "updatedAt": {},
      "url": "https://example.com",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Tales action reference](actions/list-tales.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tAYL/latest/actions/list-tales).

## Create Tale From Text



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/create-tale-from-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "markup": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/create-tale-from-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "markup": "string"
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
      "taleId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Tale From Text action reference](actions/create-tale-from-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tAYL/latest/actions/create-tale-from-text).
