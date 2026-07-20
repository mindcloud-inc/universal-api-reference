# Wistia: Get Folder

Retrieves a single folder from Wistia.

```
GET https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-folder?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-folder?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anonymousCanDownload` | boolean |  |
| `anonymousCanUpload` | boolean |  |
| `created` | date | The date that the folder was originally created. |
| `cursor` | string | A cursor for stable pagination based on current `sort_by` order. You can pass this to `cursor[before]` or `cursor[after]` as a parameter to fetch the records before or after this record in the same sort order. This is only populated if records were fetched with `cursor[enabled]`, or `cursor[before]` or `cursor[after]`. |
| `description` | string | The folder’s description. |
| `hashedId` | string | A private hashed id, uniquely identifying the folder within the system. |
| `id` | number | A unique numeric identifier for the folder within the system. |
| `mediaCount` | number | The number of different medias that have been uploaded to the folder. |
| `medias` | object | A link to where you can fetch the medias for this folder. |
| `medias.archived` | boolean | Whether or not the media is archived, either true or false. |
| `medias.created` | date | The date when the media was originally uploaded. |
| `medias.description` | string | A description for the media which usually appears near the top of the sidebar on the media's page. |
| `medias.duration` | number |  |
| `medias.embedCode` | string | DEPRECATED: If you want to programmatically embed videos, follow the construct an embed code guide. |
| `medias.hashedId` | string | A unique alphanumeric identifier for this media. |
| `medias.id` | number | A unique numeric identifier for the media within the system. |
| `medias.name` | string | The display name of the media. |
| `medias.progress` | number | A floating point value between 0 and 1 that indicates the progress of the processing for this file. |
| `medias.section` | string |  |
| `medias.status` | string | Post upload processing status. - `queued`: the file is waiting in the queue to be processed. - `processing`: the file is actively being processed. - `ready`: the file has been fully processed and is ready for embedding and viewing. - `failed`: the file was unable to be processed (usually a format or size error). |
| `medias.thumbnail` | object |  |
| `medias.thumbnail.height` | number |  |
| `medias.thumbnail.url` | string |  |
| `medias.thumbnail.width` | number |  |
| `medias.type` | string | A string representing what type of media this is. |
| `medias.updated` | date | The date when the media was last changed. |
| `name` | string | The folder’s display name. |
| `public` | boolean | A boolean indicating whether the folder is available for public (anonymous) viewing. |
| `publicId` | string | If the folder is public, this field contains a string representing the ID used for referencing the folder in public URLs. |
| `updated` | date | The date that the folder was last updated. |

## Native endpoint

Through the native Wistia API, this operation is `GET /v1/projects/:id` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

