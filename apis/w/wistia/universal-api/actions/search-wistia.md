# Wistia: Search Wistia

Finds folders, media, and webinars in Wistia.

```
GET https://connect.mindcloud.co/v1/universal/wistia/latest/actions/search-wistia
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/search-wistia?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/search-wistia?${params}`, {
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
| `query` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "channelEpisodes": [
          {
            "channelHashedId": "string",
            "created": "2026-05-07T12:00:00.000Z",
            "description": "string",
            "hashedId": "string",
            "id": 1,
            "mediaHashedId": "string",
            "publishAt": "2026-05-07T12:00:00.000Z",
            "published": true,
            "summary": "string",
            "title": "string",
            "updated": "2026-05-07T12:00:00.000Z"
          }
        ],
        "channels": [
          {
            "created": "2026-05-07T12:00:00.000Z",
            "description": "string",
            "hashedId": "string",
            "id": 1,
            "mediaCount": 1,
            "name": "Ava Chen",
            "updated": "2026-05-07T12:00:00.000Z"
          }
        ],
        "folders": [
          {
            "anonymousCanDownload": true,
            "anonymousCanUpload": true,
            "created": "2026-05-07T12:00:00.000Z",
            "cursor": "string",
            "description": "string",
            "hashedId": "string",
            "id": 1,
            "mediaCount": 1,
            "medias": {
              "archived": true,
              "created": "2026-05-07T12:00:00.000Z",
              "description": "string",
              "duration": 1,
              "embedCode": "string",
              "hashedId": "string",
              "id": 1,
              "name": "Ava Chen",
              "progress": 1,
              "section": "string",
              "status": "string",
              "thumbnail": {
                "height": 1,
                "url": "https://example.com",
                "width": 1
              },
              "type": "string",
              "updated": "2026-05-07T12:00:00.000Z"
            },
            "name": "Ava Chen",
            "public": true,
            "publicId": "string",
            "updated": "2026-05-07T12:00:00.000Z"
          }
        ],
        "medias": [
          {
            "archived": true,
            "created": "2026-05-07T12:00:00.000Z",
            "description": "string",
            "duration": 1,
            "embedCode": "string",
            "folderHashedId": "string",
            "hashedId": "string",
            "id": 1,
            "name": "Ava Chen",
            "progress": 1,
            "section": "string",
            "status": "string",
            "thumbnail": {
              "height": 1,
              "url": "https://example.com",
              "width": 1
            },
            "type": "string",
            "updated": "2026-05-07T12:00:00.000Z"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.channelEpisodes` | array<object> |  |
| `data.channelEpisodes[].channelHashedId` | string | The hashed ID of the channel this episode belongs to. |
| `data.channelEpisodes[].created` | date | The date when the channel episode was originally created. |
| `data.channelEpisodes[].description` | string | The episode notes for the channel episode. |
| `data.channelEpisodes[].hashedId` | string | A unique alphanumeric identifier for this channel episode. |
| `data.channelEpisodes[].id` | number | A unique numeric identifier for the channel episode within the system. |
| `data.channelEpisodes[].mediaHashedId` | string | The hashed ID of the media associated with this channel episode. |
| `data.channelEpisodes[].publishAt` | date | The scheduled publish date (only present if scheduled). |
| `data.channelEpisodes[].published` | boolean | Whether the channel episode is published. |
| `data.channelEpisodes[].summary` | string | The description of the channel episode. |
| `data.channelEpisodes[].title` | string | The title of the channel episode. |
| `data.channelEpisodes[].updated` | date | The date when the channel episode was last updated. |
| `data.channels` | array<object> |  |
| `data.channels[].created` | date | The date when the channel was originally created. |
| `data.channels[].description` | string | The channel's description. |
| `data.channels[].hashedId` | string | A unique alphanumeric identifier for this channel. |
| `data.channels[].id` | number | A unique numeric identifier for the channel within the system. |
| `data.channels[].mediaCount` | number | The number of medias in the channel. |
| `data.channels[].name` | string | The display name for the channel. |
| `data.channels[].updated` | date | The date when the channel was last updated. |
| `data.folders` | array<object> |  |
| `data.folders[].anonymousCanDownload` | boolean |  |
| `data.folders[].anonymousCanUpload` | boolean |  |
| `data.folders[].created` | date | The date that the folder was originally created. |
| `data.folders[].cursor` | string | A cursor for stable pagination based on current `sort_by` order. You can pass this to `cursor[before]` or `cursor[after]` as a parameter to fetch the records before or after this record in the same sort order. This is only populated if records were fetched with `cursor[enabled]`, or `cursor[before]` or `cursor[after]`. |
| `data.folders[].description` | string | The folder’s description. |
| `data.folders[].hashedId` | string | A private hashed id, uniquely identifying the folder within the system. |
| `data.folders[].id` | number | A unique numeric identifier for the folder within the system. |
| `data.folders[].mediaCount` | number | The number of different medias that have been uploaded to the folder. |
| `data.folders[].medias` | object | A link to where you can fetch the medias for this folder. |
| `data.folders[].medias.archived` | boolean | Whether or not the media is archived, either true or false. |
| `data.folders[].medias.created` | date | The date when the media was originally uploaded. |
| `data.folders[].medias.description` | string | A description for the media which usually appears near the top of the sidebar on the media's page. |
| `data.folders[].medias.duration` | number |  |
| `data.folders[].medias.embedCode` | string | DEPRECATED: If you want to programmatically embed videos, follow the construct an embed code guide. |
| `data.folders[].medias.hashedId` | string | A unique alphanumeric identifier for this media. |
| `data.folders[].medias.id` | number | A unique numeric identifier for the media within the system. |
| `data.folders[].medias.name` | string | The display name of the media. |
| `data.folders[].medias.progress` | number | A floating point value between 0 and 1 that indicates the progress of the processing for this file. |
| `data.folders[].medias.section` | string |  |
| `data.folders[].medias.status` | string | Post upload processing status. - `queued`: the file is waiting in the queue to be processed. - `processing`: the file is actively being processed. - `ready`: the file has been fully processed and is ready for embedding and viewing. - `failed`: the file was unable to be processed (usually a format or size error). |
| `data.folders[].medias.thumbnail` | object |  |
| `data.folders[].medias.thumbnail.height` | number |  |
| `data.folders[].medias.thumbnail.url` | string |  |
| `data.folders[].medias.thumbnail.width` | number |  |
| `data.folders[].medias.type` | string | A string representing what type of media this is. |
| `data.folders[].medias.updated` | date | The date when the media was last changed. |
| `data.folders[].name` | string | The folder’s display name. |
| `data.folders[].public` | boolean | A boolean indicating whether the folder is available for public (anonymous) viewing. |
| `data.folders[].publicId` | string | If the folder is public, this field contains a string representing the ID used for referencing the folder in public URLs. |
| `data.folders[].updated` | date | The date that the folder was last updated. |
| `data.medias` | array<object> |  |
| `data.medias[].archived` | boolean | Whether or not the media is archived, either true or false. |
| `data.medias[].created` | date | The date when the media was originally uploaded. |
| `data.medias[].description` | string | A description for the media which usually appears near the top of the sidebar on the media's page. |
| `data.medias[].duration` | number |  |
| `data.medias[].embedCode` | string | DEPRECATED: If you want to programmatically embed videos, follow the construct an embed code guide. |
| `data.medias[].folderHashedId` | string | The hashed ID of the folder this media belongs to |
| `data.medias[].hashedId` | string | A unique alphanumeric identifier for this media. |
| `data.medias[].id` | number | A unique numeric identifier for the media within the system. |
| `data.medias[].name` | string | The display name of the media. |
| `data.medias[].progress` | number | A floating point value between 0 and 1 that indicates the progress of the processing for this file. |
| `data.medias[].section` | string |  |
| `data.medias[].status` | string | Post upload processing status. - `queued`: the file is waiting in the queue to be processed. - `processing`: the file is actively being processed. - `ready`: the file has been fully processed and is ready for embedding and viewing. - `failed`: the file was unable to be processed (usually a format or size error). |
| `data.medias[].thumbnail` | object |  |
| `data.medias[].thumbnail.height` | number |  |
| `data.medias[].thumbnail.url` | string |  |
| `data.medias[].thumbnail.width` | number |  |
| `data.medias[].type` | string | A string representing what type of media this is. |
| `data.medias[].updated` | date | The date when the media was last changed. |

## Native endpoint

Through the native Wistia API, this operation is `GET /modern/search` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-wistia.md) for the provider-specific parameters and requirements.

