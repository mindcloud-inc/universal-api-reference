# Typlog: Create Episode

Creates a new episode in Typlog.

```
POST https://connect.mindcloud.co/v1/universal/typlog/latest/actions/create-episode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typlog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/create-episode" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "4863",
  "title": "Episode One",
  "slug": "episode-one",
  "lang": "en",
  "format": "markdown"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/typlog/latest/actions/create-episode', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "4863",
    "title": "Episode One",
    "slug": "episode-one",
    "lang": "en",
    "format": "markdown"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | number | yes | Typlog site ID used to set the X-Site-Id header. Example: `4863`. |
| `title` | string | yes | Episode title. Example: `Episode One`. |
| `slug` | string | yes | Episode slug. Example: `episode-one`. |
| `lang` | string | yes | Episode language code. Example: `en`. |
| `format` | string | yes | Episode content format. Example: `markdown`. |
| `subtitle` | string | no | Episode subtitle. |
| `visibility` | string | no | Episode visibility. Example: `public`. |
| `comment` | string | no | Comment setting. Example: `open`. |
| `season` | number | no | Season number. |
| `episode` | number | no | Episode number. |
| `explicit` | boolean | no | Whether the episode is explicit. |
| `episodeType` | string | no | Episode type. Example: `full`. |
| `tags[]` | array<number> | no | Tag IDs. |
| `hosts[]` | array<number> | no | Host author IDs. |
| `guests[]` | array<number> | no | Guest author IDs. |

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

Through the native Typlog API, this operation is `POST /episodes` (base URL `https://api.typlog.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-episode.md) for the provider-specific parameters and requirements.

