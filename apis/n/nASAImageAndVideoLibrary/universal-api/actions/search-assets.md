# NASA Image and Video Library: Search Assets

Finds assets in NASA Image and Video Library by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/search-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NASA Image and Video Library `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/search-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/search-assets?${params}`, {
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
| `q` | string | no | Free text terms to match across indexed NASA media metadata. Provide at least one search parameter somewhere in this action. |
| `nasaId` | string | no | Restrict results to a specific NASA media asset ID. |
| `mediaType` | string | no | Comma-separated media types to return. Available values: image, video, audio. |
| `title` | string | no | Terms to search within asset titles. |
| `description` | string | no | Terms to search within asset descriptions. |
| `keywords` | string | no | Comma-separated keywords to search within asset keyword metadata. |
| `center` | string | no | Restrict results to a specific NASA center code such as JSC, KSC, or HQ. |
| `location` | string | no | Terms to search within asset location metadata. |
| `photographer` | string | no | Restrict results by the primary photographer name. |
| `yearStart` | string | no | Restrict results to assets created on or after this year. Format: YYYY. |
| `yearEnd` | string | no | Restrict results to assets created on or before this year. Format: YYYY. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Page number to retrieve. Starts at 1. |
| `pageSize` | number | no | Number of results per page. NASA documents a default of 100. |
| `description508` | string | no | Terms to search within accessibility 508 descriptions. |
| `secondaryCreator` | string | no | Restrict results by a secondary photographer or videographer name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": {
        "href": "string",
        "items": [
          {
            "data": [
              {
                "center": "string",
                "date_created": "2026-05-07T12:00:00.000Z",
                "description": "string",
                "keywords": [
                  "string"
                ],
                "location": "string",
                "media_type": "string",
                "nasa_id": "string",
                "photographer": "string",
                "title": "string"
              }
            ],
            "href": "string",
            "links": [
              {}
            ]
          }
        ],
        "links": [
          {}
        ],
        "metadata": {
          "total_hits": 1
        },
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection.href` | string | Canonical NASA URL for this search result page. |
| `collection.items` | array<object> | Search result items returned for this page. |
| `collection.items[].data` | array<object> | Metadata objects describing the result asset. |
| `collection.items[].data[].center` | string | NASA center associated with the asset. |
| `collection.items[].data[].date_created` | date | Asset creation date returned by NASA. |
| `collection.items[].data[].description` | string | Asset description. |
| `collection.items[].data[].keywords` | array<string> | Keywords attached to the asset. |
| `collection.items[].data[].location` | string | Location metadata for the asset. |
| `collection.items[].data[].media_type` | string | Media type such as image, video, or audio. |
| `collection.items[].data[].nasa_id` | string | NASA asset identifier. |
| `collection.items[].data[].photographer` | string | Primary photographer name when present. |
| `collection.items[].data[].title` | string | Asset title. |
| `collection.items[].href` | string | Asset collection URL for one search result. |
| `collection.items[].links` | array<object> | Preview and related asset links. |
| `collection.links` | array<object> | Pagination links such as next or previous. |
| `collection.metadata.total_hits` | number | Total number of matching assets across all pages. |
| `collection.version` | string | Collection+JSON version returned by NASA. |

## Native endpoint

Through the native NASA Image and Video Library API, this operation is `GET /search` (base URL `https://images-api.nasa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-assets.md) for the provider-specific parameters and requirements.

