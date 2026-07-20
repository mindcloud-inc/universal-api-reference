# Typlog: Get Episode

Retrieves a Typlog episode by ID.

```
GET https://connect.mindcloud.co/v1/universal/typlog/latest/actions/get-episode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typlog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/get-episode?connectionId=$CONNECTION_ID&id=1&siteId=4863" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "siteId": "4863"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typlog/latest/actions/get-episode?${params}`, {
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
| `id` | number | yes | ID of the episode. Example: `1`. |
| `siteId` | number | yes | Typlog site ID used to set the X-Site-Id header. Example: `4863`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio": {},
      "author": "string",
      "comment": "string",
      "content": "string",
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
      "metadata": {},
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
| `content` | string |  |
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
| `metadata` | object |  |
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

Through the native Typlog API, this operation is `GET /episodes/[:id]` (base URL `https://api.typlog.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-episode.md) for the provider-specific parameters and requirements.

