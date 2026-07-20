# Storyblok: Get Story from Release

Retrieves a Storyblok story from a specific release.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-story-from-release
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-story-from-release?connectionId=$CONNECTION_ID&storyId=home&releaseId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storyId": "home",
  "releaseId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-story-from-release?${params}`, {
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
| `storyId` | string | yes | The story slug or ID to retrieve from a release. Default: `home`. |
| `releaseId` | string | yes | The release ID to read the story from. Default: `1`. |
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
      "story": {
        "content": {},
        "full_slug": "string",
        "id": 1,
        "lang": "string",
        "name": "Ava Chen",
        "release_id": 1,
        "slug": "string",
        "uuid": "string"
      }
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
| `story` | object | The requested story from the selected release. |
| `story.content` | object | The story content payload. |
| `story.full_slug` | string | The full story slug. |
| `story.id` | number | The story ID. |
| `story.lang` | string | The story language. |
| `story.name` | string | The story name. |
| `story.release_id` | number | The release ID when present. |
| `story.slug` | string | The story slug. |
| `story.uuid` | string | The story UUID. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /stories/:storyId` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-story-from-release.md) for the provider-specific parameters and requirements.

