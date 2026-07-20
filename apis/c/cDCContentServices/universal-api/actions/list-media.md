# CDC Content Services: List Media

Retrieves media from CDC Content Services.

```
GET https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CDC Content Services `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-media?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cDCContentServices/latest/actions/list-media?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | no | Search topic, name, and description. Use quotes for exact phrase matching. |
| `nameContains` | string | no | Return media whose name contains this value. |
| `topic` | string | no | Filter media by topic name. |
| `audience` | string | no | Filter media by audience name. |
| `languageName` | string | no | Filter media by language name, such as English or Spanish. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaTypes` | string | no | Comma-separated media type names, such as HTML, Image, Video, Button, Badge, Widget, or Infographic. |
| `topicIds` | string | no | Comma-separated CDC topic identifiers. |
| `sourceAcronym` | string | no | Filter media by source acronym, such as CDC. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternateImages` | array<object> | Alternate image renditions. |
| `alternateText` | string | Alternate text. |
| `attribution` | string | CDC attribution HTML. |
| `author` | string | Author value from CDC metadata. |
| `campaigns` | array<object> | Campaign metadata. |
| `childCount` | number | Number of child media items. |
| `contentUrl` | string | CDC content endpoint URL. |
| `dataSize` | string | Data size value. |
| `dateContentAuthored` | date | Content authored timestamp. |
| `dateContentPublished` | date | Content published timestamp. |
| `dateContentReviewed` | date | Content reviewed timestamp. |
| `dateContentUpdated` | date | Content updated timestamp. |
| `dateModified` | date | Modified timestamp. |
| `datePublished` | date | Published timestamp. |
| `dateSyndicationCaptured` | date | Syndication captured timestamp. |
| `dateSyndicationUpdated` | date | Syndication updated timestamp. |
| `dateSyndicationVisible` | date | Syndication visible timestamp. |
| `description` | string | Media description. |
| `domainName` | string | Associated domain name. |
| `embedCode` | string | CDC embed code. |
| `embedUrl` | string | CDC embed endpoint URL. |
| `enclosures` | array<object> | Enclosure metadata. |
| `extendedAttributes` | object | Extended CDC attributes. |
| `extension` | object | Extension metadata. |
| `featuredText` | string | Featured text. |
| `geoTags` | array<object> | Geographic tags attached to the media item. |
| `id` | number | CDC media identifier from runtime. |
| `isTopSyndicated` | string | CDC top-syndicated flag value. |
| `language` | object | Language metadata. |
| `length` | string | Length value from CDC metadata. |
| `maintainingOrgId` | string | Maintaining organization identifier. |
| `maintainingOrgName` | string | Maintaining organization name. |
| `mediaType` | string | CDC media type. |
| `name` | string | Media title/name. |
| `noScriptText` | string | No-script fallback text. |
| `owningOrgId` | string | Owning organization identifier. |
| `owningOrgName` | string | Owning organization name. |
| `pageCount` | string | Page count value. |
| `parentCount` | number | Number of parent media items. |
| `parents` | array<object> | Parent media items. |
| `persistentUrl` | string | Persistent CDC API URL. |
| `persistentUrlToken` | string | Persistent URL token. |
| `source` | object | Source metadata. |
| `sourceUrl` | string | Original CDC source URL. |
| `status` | string | Publication status. |
| `syndicateUrl` | string | CDC syndication endpoint URL. |
| `tags` | array<object> | Tags attached to the media item. |
| `targetUrl` | string | Target URL for the media item. |
| `thumbnailUrl` | string | Thumbnail image URL. |
| `url` | string | CDC API URL for this media resource. |

## Native endpoint

Through the native CDC Content Services API, this operation is `GET /v2/resources/media` (base URL `https://tools.cdc.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-media.md) for the provider-specific parameters and requirements.

