# Wistia: Update Media

Updates an existing media item in Wistia.

```
PUT https://connect.mindcloud.co/v1/universal/wistia/latest/actions/update-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/update-media" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaHashedId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wistia/latest/actions/update-media', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaHashedId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaHashedId` | string | yes |  |
| `name` | string | no |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `created` | date | The date when the media was originally uploaded. |
| `description` | string | A description for the media which usually appears near the top of the sidebar on the media's page. |
| `duration` | number |  |
| `embedCode` | string | DEPRECATED: If you want to programmatically embed videos, follow the construct an embed code guide. |
| `hashedId` | string | A unique alphanumeric identifier for this media. |
| `id` | number | A unique numeric identifier for the media within the system. |
| `name` | string | The display name of the media. |
| `progress` | number | A floating point value between 0 and 1 that indicates the progress of the processing for this file. |
| `section` | string |  |
| `status` | string | Post upload processing status. - `queued`: the file is waiting in the queue to be processed. - `processing`: the file is actively being processed. - `ready`: the file has been fully processed and is ready for embedding and viewing. - `failed`: the file was unable to be processed (usually a format or size error). |
| `tags` | array<object> | Tags associated with this media. |
| `tags[].name` | string | The display name of the tag. |
| `thumbnail` | object |  |
| `thumbnail.height` | number |  |
| `thumbnail.url` | string |  |
| `thumbnail.width` | number |  |
| `type` | string | A string representing what type of media this is. |
| `updated` | date | The date when the media was last changed. |

## Native endpoint

Through the native Wistia API, this operation is `PUT /modern/medias/:mediaHashedId` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-media.md) for the provider-specific parameters and requirements.

