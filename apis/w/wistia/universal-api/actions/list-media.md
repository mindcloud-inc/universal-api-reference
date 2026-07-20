# Wistia: List Media

Retrieves media from the Wistia account.

```
GET https://connect.mindcloud.co/v1/universal/wistia/latest/actions/list-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/list-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/list-media?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "assets": [
        {
          "contentType": "string",
          "fileSize": 1,
          "height": 1,
          "type": "string",
          "url": "https://example.com",
          "width": 1
        }
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "cursor": "string",
      "description": "string",
      "duration": 1,
      "embedCode": "string",
      "folder": {
        "hashedId": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "hashedId": "string",
      "id": 1,
      "name": "Ava Chen",
      "progress": 1,
      "section": "string",
      "status": "string",
      "subfolder": {
        "created": "2026-05-07T12:00:00.000Z",
        "cursor": "string",
        "description": "string",
        "hashedId": "string",
        "name": "Ava Chen",
        "position": 1,
        "updated": "2026-05-07T12:00:00.000Z"
      },
      "tags": [
        {
          "name": "Ava Chen"
        }
      ],
      "thumbnail": {
        "height": 1,
        "url": "https://example.com",
        "width": 1
      },
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether or not the media is archived, either true or false. |
| `assets` | array<object> | An array of the assets available for this media. |
| `assets[].contentType` | string |  |
| `assets[].fileSize` | number |  |
| `assets[].height` | number |  |
| `assets[].type` | string | The internal type of the asset, describing how the asset should be used. Values can include OriginalFile, FlashVideoFile, MdFlashVideoFile, HdFlashVideoFile, Mp4VideoFile, MdMp4VideoFile, HdMp4VideoFile, IPhoneVideoFile, StillImageFile, SwfFile, Mp3AudioFile, and LargeImageFile. |
| `assets[].url` | string | A direct-access URL to the content of the asset. |
| `assets[].width` | number |  |
| `created` | date | The date when the media was originally uploaded. |
| `cursor` | string | A cursor for stable pagination based on current `sort_by` order. You can pass this to `cursor[before]` or `cursor[after]` as a parameter to fetch the records before or after this record in the same sort order. This is only populated if records were fetched with `cursor[enabled]`, or `cursor[before]` or `cursor[after]`. |
| `description` | string | A description for the media which usually appears near the top of the sidebar on the media's page. |
| `duration` | number |  |
| `embedCode` | string | DEPRECATED: If you want to programmatically embed videos, follow the construct an embed code guide. |
| `folder` | object |  |
| `folder.hashedId` | string | A private hashed id, uniquely identifying the folder within the system. |
| `folder.id` | number | A unique numeric identifier for the folder within the system. |
| `folder.name` | string | The folder’s display name. |
| `hashedId` | string | A unique alphanumeric identifier for this media. |
| `id` | number | A unique numeric identifier for the media within the system. |
| `name` | string | The display name of the media. |
| `progress` | number | A floating point value between 0 and 1 that indicates the progress of the processing for this file. |
| `section` | string |  |
| `status` | string | Post upload processing status. - `queued`: the file is waiting in the queue to be processed. - `processing`: the file is actively being processed. - `ready`: the file has been fully processed and is ready for embedding and viewing. - `failed`: the file was unable to be processed (usually a format or size error). |
| `subfolder` | object | A subfolder within a folder that contains media. |
| `subfolder.created` | date | The date when the subfolder was created. |
| `subfolder.cursor` | string | A cursor for stable pagination based on current `sort_by` order. You can pass this to `cursor[before]` or `cursor[after]` as a parameter to fetch the records before or after this record in the same sort order. This is only populated if records were fetched with `cursor[enabled]`, or `cursor[before]` or `cursor[after]`. |
| `subfolder.description` | string | A description for the subfolder. |
| `subfolder.hashedId` | string | A unique alphanumeric identifier for this subfolder. |
| `subfolder.name` | string | The display name of the subfolder. |
| `subfolder.position` | number | The position of this subfolder within its folder, used for ordering. |
| `subfolder.updated` | date | The date when the subfolder was last modified. |
| `tags` | array<object> | Tags associated with this media. |
| `tags[].name` | string | The display name of the tag. |
| `thumbnail` | object |  |
| `thumbnail.height` | number |  |
| `thumbnail.url` | string |  |
| `thumbnail.width` | number |  |
| `type` | string | A string representing what type of media this is. |
| `updated` | date | The date when the media was last changed. |

## Native endpoint

Through the native Wistia API, this operation is `GET /modern/medias` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-media.md) for the provider-specific parameters and requirements.

