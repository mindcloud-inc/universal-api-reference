# Typeflo: List Posts

Retrieves published blog posts from Typeflo.

```
GET https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeflo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/list-posts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/list-posts?${params}`, {
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
| `slug` | string | no | Filter posts by their unique slug. |
| `author` | string | no | Filter posts by author ID. |
| `title` | string | no | Filter posts by title. |
| `tocStatus` | boolean | no | Filter posts by table-of-contents status. |
| `restrictionStatus` | boolean | no | Filter posts by content restriction status. |
| `restrictionPercentage` | number | no | Filter posts by restriction percentage. |
| `isDraft` | boolean | no | Filter posts by draft status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "categories": [
        {}
      ],
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "docsid": "string",
      "excerpt": "string",
      "featuredImage": {},
      "id": "string",
      "isDraft": true,
      "metadescription": "string",
      "metatitle": "string",
      "opengraph": {},
      "readingTime": "string",
      "restriction": {},
      "scheduled": "string",
      "slug": "string",
      "tags": [
        {}
      ],
      "title": "string",
      "tocStatus": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `categories` | array<object> |  |
| `content` | string |  |
| `createdAt` | date |  |
| `docsid` | string |  |
| `excerpt` | string |  |
| `featuredImage` | object |  |
| `id` | string |  |
| `isDraft` | boolean |  |
| `metadescription` | string |  |
| `metatitle` | string |  |
| `opengraph` | object |  |
| `readingTime` | string |  |
| `restriction` | object |  |
| `scheduled` | string |  |
| `slug` | string |  |
| `tags` | array<object> |  |
| `title` | string |  |
| `tocStatus` | boolean |  |

## Native endpoint

Through the native Typeflo API, this operation is `GET /content/posts` (base URL `https://{{credentials.subdomain}}.typeflo.io/api/headless`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

