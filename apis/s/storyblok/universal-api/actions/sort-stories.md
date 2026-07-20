# Storyblok: Sort Stories

Retrieves Storyblok stories sorted by story properties.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/sort-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/sort-stories?connectionId=$CONNECTION_ID&limit=25&offset=0&sortBy=position%3Aasc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "sortBy": "position:asc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/sort-stories?${params}`, {
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
| `sortBy` | string | yes | The Storyblok sort expression to apply, such as `created_at:desc`. Default: `position:asc`. |
| `version` | string | no | Whether to read draft or published content. Default: `draft`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cv": 1,
      "links": [
        {}
      ],
      "rels": [
        {}
      ],
      "stories": [
        {
          "content": {},
          "id": 1,
          "lang": "string",
          "name": "Ava Chen",
          "position": 1,
          "slug": "string",
          "uuid": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cv` | number | The cache version. |
| `links` | array<object> | Resolved links returned by Storyblok. |
| `rels` | array<object> | Resolved relations returned by Storyblok. |
| `stories` | array<object> | Stories sorted by the requested field. |
| `stories[].content` | object | The story content payload. |
| `stories[].id` | number | The story ID. |
| `stories[].lang` | string | The story language. |
| `stories[].name` | string | The story name. |
| `stories[].position` | number | The story position. |
| `stories[].slug` | string | The story slug. |
| `stories[].uuid` | string | The story UUID. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /stories` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/sort-stories.md) for the provider-specific parameters and requirements.

