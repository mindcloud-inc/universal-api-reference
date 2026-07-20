# DatoCMS: Get Upload



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-upload?connectionId=$CONNECTION_ID&uploadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uploadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-upload?${params}`, {
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
| `uploadId` | string | yes | Upload ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "author": "string",
        "basename": "Ava Chen",
        "blurhash": "string",
        "colors": [
          {
            "alpha": 1,
            "blue": 1,
            "green": 1,
            "red": 1
          }
        ],
        "copyright": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "defaultFieldMetadata": {
          "en": {
            "alt": "string",
            "focalPoint": "string",
            "title": "string"
          }
        },
        "duration": "string",
        "filename": "Ava Chen",
        "format": "string",
        "frameRate": "string",
        "height": 1,
        "isImage": true,
        "md5": "string",
        "mimeType": "string",
        "muxMp4HighestRes": "string",
        "muxPlaybackId": "string",
        "notes": "string",
        "path": "string",
        "size": 1,
        "smartTags": [
          "string"
        ],
        "thumbhash": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com",
        "width": 1
      },
      "id": "string",
      "relationships": {
        "creator": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "uploadCollection": {
          "data": "string"
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.author` | string |  |
| `attributes.basename` | string |  |
| `attributes.blurhash` | string |  |
| `attributes.colors[].alpha` | number |  |
| `attributes.colors[].blue` | number |  |
| `attributes.colors[].green` | number |  |
| `attributes.colors[].red` | number |  |
| `attributes.copyright` | string |  |
| `attributes.createdAt` | date |  |
| `attributes.defaultFieldMetadata.en.alt` | string |  |
| `attributes.defaultFieldMetadata.en.focalPoint` | string |  |
| `attributes.defaultFieldMetadata.en.title` | string |  |
| `attributes.duration` | string |  |
| `attributes.filename` | string |  |
| `attributes.format` | string |  |
| `attributes.frameRate` | string |  |
| `attributes.height` | number |  |
| `attributes.isImage` | boolean |  |
| `attributes.md5` | string |  |
| `attributes.mimeType` | string |  |
| `attributes.muxMp4HighestRes` | string |  |
| `attributes.muxPlaybackId` | string |  |
| `attributes.notes` | string |  |
| `attributes.path` | string |  |
| `attributes.size` | number |  |
| `attributes.smartTags` | array<string> |  |
| `attributes.thumbhash` | string |  |
| `attributes.updatedAt` | date |  |
| `attributes.url` | string |  |
| `attributes.width` | number |  |
| `id` | string |  |
| `relationships.creator.data.id` | string |  |
| `relationships.creator.data.type` | string |  |
| `relationships.uploadCollection.data` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /uploads/:uploadId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload.md) for the provider-specific parameters and requirements.

