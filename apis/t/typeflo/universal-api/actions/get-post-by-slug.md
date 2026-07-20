# Typeflo: Get Post By Slug

Retrieves a published post from Typeflo by slug.

```
GET https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/get-post-by-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/get-post-by-slug?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/get-post-by-slug?${params}`, {
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
| `slug` | string | yes | The unique slug of the post. |

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

Through the native Typeflo API, this operation is `GET /content/posts/:slug` (base URL `https://{{credentials.subdomain}}.typeflo.io/api/headless`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-by-slug.md) for the provider-specific parameters and requirements.

