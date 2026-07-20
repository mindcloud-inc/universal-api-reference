# Postpone: List Media

Retrieves media from Postpone.

```
GET https://connect.mindcloud.co/v1/universal/postpone/latest/actions/list-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/list-media?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postpone/latest/actions/list-media?${params}`, {
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
| `variables.orderBy` | string | no | Sort order such as -date_created. Default: `-date_created`. |
| `variables.limit` | number | no | Maximum number of media files to return. Default: `20`. |
| `variables.page` | number | no | Page number for pagination. Default: `1`. |
| `variables.search` | string | no | Search term for media filenames. |
| `variables.fileType` | string | no | Optional file type such as IMAGE, VIDEO, GIF, or AUDIO. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "humanReadableSize": "string",
      "id": "string",
      "mimeType": "string",
      "name": "Ava Chen",
      "size": 1,
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
| `dateCreated` | date |  |
| `humanReadableSize` | string |  |
| `id` | string |  |
| `mimeType` | string |  |
| `name` | string |  |
| `size` | number |  |
| `thumbnailUrl` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-media.md) for the provider-specific parameters and requirements.

