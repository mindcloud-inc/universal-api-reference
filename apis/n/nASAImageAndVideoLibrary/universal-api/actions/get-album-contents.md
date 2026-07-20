# NASA Image and Video Library: Get Album Contents

Retrieves album contents from NASA Image and Video Library.

```
GET https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-album-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NASA Image and Video Library `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-album-contents?connectionId=$CONNECTION_ID&albumName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "albumName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-album-contents?${params}`, {
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
| `albumName` | string | yes | The case-sensitive NASA album name to retrieve. |
| `page` | number | no | Page number to retrieve. Starts at 1. |

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
| `collection.href` | string | Canonical NASA URL for this album result page. |
| `collection.items` | array<object> | Album members returned for this page. |
| `collection.items[].data` | array<object> | Metadata objects describing the album member. |
| `collection.items[].data[].center` | string | NASA center associated with the asset. |
| `collection.items[].data[].date_created` | date | Asset creation date returned by NASA. |
| `collection.items[].data[].description` | string | Asset description. |
| `collection.items[].data[].keywords` | array<string> | Keywords attached to the asset. |
| `collection.items[].data[].location` | string | Location metadata for the asset. |
| `collection.items[].data[].media_type` | string | Media type such as image, video, or audio. |
| `collection.items[].data[].nasa_id` | string | NASA asset identifier. |
| `collection.items[].data[].photographer` | string | Primary photographer name when present. |
| `collection.items[].data[].title` | string | Asset title. |
| `collection.items[].href` | string | Asset collection URL for one album member. |
| `collection.items[].links` | array<object> | Preview and related asset links. |
| `collection.links` | array<object> | Pagination links such as next or previous. |
| `collection.metadata.total_hits` | number | Total number of album members across all pages. |
| `collection.version` | string | Collection+JSON version returned by NASA. |

## Native endpoint

Through the native NASA Image and Video Library API, this operation is `GET /album/:album_name` (base URL `https://images-api.nasa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-album-contents.md) for the provider-specific parameters and requirements.

