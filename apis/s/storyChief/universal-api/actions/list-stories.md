# StoryChief: List Stories

Retrieves stories from StoryChief.

```
GET https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/list-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a StoryChief `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/list-stories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/list-stories?${params}`, {
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
| `language` | string | no | Language selector documented as lang. |
| `status` | string | no | Story status selector documented as status. Default: `all`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceId` | number | no | Source ID selector documented as source. |
| `updatedAfter` | date | no | Only return stories updated after this timestamp. |
| `authorId` | number | no | Author ID selector documented as author_id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dueAt": {},
      "editUrl": "https://example.com",
      "excerpt": {},
      "id": 1,
      "language": {},
      "publishedAt": {},
      "seoDescription": {},
      "seoKeyword": {},
      "seoTitle": {},
      "slug": "string",
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dueAt` | object |  |
| `editUrl` | string |  |
| `excerpt` | object |  |
| `id` | number |  |
| `language` | object |  |
| `publishedAt` | object |  |
| `seoDescription` | object |  |
| `seoKeyword` | object |  |
| `seoTitle` | object |  |
| `slug` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native StoryChief API, this operation is `GET /stories` (base URL `https://api.storychief.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stories.md) for the provider-specific parameters and requirements.

