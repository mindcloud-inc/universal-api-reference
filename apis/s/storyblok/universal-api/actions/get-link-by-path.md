# Storyblok: Get Link by UUID

Retrieves a Storyblok link by UUID.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-link-by-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-link-by-path?connectionId=$CONNECTION_ID&linkId=5bc3a004-367a-4a89-a4bf-5330441590ff" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "5bc3a004-367a-4a89-a4bf-5330441590ff"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-link-by-path?${params}`, {
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
| `linkId` | string | yes | The Storyblok link UUID. Default: `5bc3a004-367a-4a89-a4bf-5330441590ff`. |
| `version` | string | no | Whether to read draft or published content. Default: `draft`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": {
        "id": 1,
        "is_folder": true,
        "is_startpage": true,
        "name": "https://example.com",
        "parent_id": 1,
        "path": "https://example.com",
        "position": 1,
        "published": true,
        "slug": "https://example.com",
        "uuid": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | object | The requested link. |
| `link.id` | number | The linked story ID. |
| `link.is_folder` | boolean | Whether the link points to a folder. |
| `link.is_startpage` | boolean | Whether the link is a start page. |
| `link.name` | string | The link name. |
| `link.parent_id` | number | The parent story ID. |
| `link.path` | string | The configured path when present. |
| `link.position` | number | The link position. |
| `link.published` | boolean | Whether the link is published. |
| `link.slug` | string | The link slug. |
| `link.uuid` | string | The link UUID. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /links/:linkId` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-by-path.md) for the provider-specific parameters and requirements.

