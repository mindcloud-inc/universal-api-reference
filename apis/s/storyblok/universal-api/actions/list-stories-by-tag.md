# Storyblok: List Stories by Tag

Retrieves Storyblok stories with a specific tag.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-stories-by-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-stories-by-tag?connectionId=$CONNECTION_ID&limit=25&offset=0&withTag=example-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "withTag": "example-tag"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-stories-by-tag?${params}`, {
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
| `withTag` | string | yes | Only return stories with this tag. Default: `example-tag`. |

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
          "slug": "string",
          "tag_list": [
            "string"
          ],
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
| `stories` | array<object> | Stories matching the requested tag. |
| `stories[].content` | object | The story content payload. |
| `stories[].id` | number | The story ID. |
| `stories[].lang` | string | The story language. |
| `stories[].name` | string | The story name. |
| `stories[].slug` | string | The story slug. |
| `stories[].tag_list` | array<string> | Tags assigned to the story. |
| `stories[].uuid` | string | The story UUID. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /stories` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stories-by-tag.md) for the provider-specific parameters and requirements.

