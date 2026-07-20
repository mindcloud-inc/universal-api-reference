# Typlog: List Episodes

Retrieves episodes from Typlog.

```
GET https://connect.mindcloud.co/v1/universal/typlog/latest/actions/list-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typlog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/list-episodes?connectionId=$CONNECTION_ID&siteId=4863" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "4863"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typlog/latest/actions/list-episodes?${params}`, {
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
| `siteId` | number | yes | Typlog site ID used to set the X-Site-Id header. Example: `4863`. |
| `cursor` | number | no | Pagination cursor. Example: `0`. |
| `search` | string | no | Search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio": {},
      "author": "string",
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "episode": 1,
      "episodeType": "string",
      "explicit": true,
      "format": "string",
      "guests": [
        {}
      ],
      "hosts": [
        {}
      ],
      "id": 1,
      "image": "string",
      "lang": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "season": 1,
      "slug": "string",
      "status": "string",
      "subtitle": "string",
      "tags": [
        {}
      ],
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio` | object |  |
| `author` | string |  |
| `comment` | string |  |
| `createdAt` | date |  |
| `episode` | number |  |
| `episodeType` | string |  |
| `explicit` | boolean |  |
| `format` | string |  |
| `guests` | array<object> |  |
| `hosts` | array<object> |  |
| `id` | number |  |
| `image` | string |  |
| `lang` | string |  |
| `publishedAt` | date |  |
| `season` | number |  |
| `slug` | string |  |
| `status` | string |  |
| `subtitle` | string |  |
| `tags` | array<object> |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Typlog API, this operation is `GET /episodes` (base URL `https://api.typlog.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episodes.md) for the provider-specific parameters and requirements.

