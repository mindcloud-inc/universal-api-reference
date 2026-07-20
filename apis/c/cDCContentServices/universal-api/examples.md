# CDC Content Services Universal API Examples

These examples use the MindCloud API key and CDC Content Services connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Media

Retrieves media from CDC Content Services by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/get-media?connectionId=$CONNECTION_ID&mediaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/get-media?${params}`, {
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
      "alternateImages": [
        {}
      ],
      "alternateText": "string",
      "attribution": "string",
      "author": "string",
      "campaigns": [
        {}
      ],
      "childCount": 1,
      "contentUrl": "https://example.com",
      "dataSize": "string",
      "dateContentAuthored": "2026-05-07T12:00:00.000Z",
      "dateContentPublished": "2026-05-07T12:00:00.000Z",
      "dateContentReviewed": "2026-05-07T12:00:00.000Z",
      "dateContentUpdated": "2026-05-07T12:00:00.000Z",
      "dateModified": "2026-05-07T12:00:00.000Z",
      "datePublished": "2026-05-07T12:00:00.000Z",
      "dateSyndicationCaptured": "2026-05-07T12:00:00.000Z",
      "dateSyndicationUpdated": "2026-05-07T12:00:00.000Z",
      "dateSyndicationVisible": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domainName": "Ava Chen",
      "embedCode": "string",
      "embedUrl": "https://example.com",
      "enclosures": [
        {}
      ],
      "extendedAttributes": {},
      "extension": {},
      "featuredText": "string",
      "geoTags": [
        {}
      ],
      "id": 1,
      "isTopSyndicated": "string",
      "language": {},
      "length": "string",
      "maintainingOrgId": "string",
      "maintainingOrgName": "Ava Chen",
      "mediaType": "string",
      "name": "Ava Chen",
      "noScriptText": "string",
      "owningOrgId": "string",
      "owningOrgName": "Ava Chen",
      "pageCount": "string",
      "parentCount": 1,
      "parents": [
        {}
      ],
      "persistentUrl": "https://example.com",
      "persistentUrlToken": "https://example.com",
      "source": {},
      "sourceUrl": "https://example.com",
      "status": "string",
      "syndicateUrl": "https://example.com",
      "tags": [
        {}
      ],
      "targetUrl": "https://example.com",
      "thumbnailUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Media action reference](actions/get-media.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cDCContentServices/latest/actions/get-media).
