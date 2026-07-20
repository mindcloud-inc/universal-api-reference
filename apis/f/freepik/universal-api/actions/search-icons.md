# Freepik: Search Icons

Finds Freepik icons by search term and filters.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-icons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-icons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-icons?${params}`, {
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
| `term` | string | no | Icon search term. Default: `instagram`. |
| `perPage` | number | no | Number of icons to return per page. Default: `1`. |
| `page` | number | no | One-based icons page to request. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "created": "2026-05-07T12:00:00.000Z",
      "family": {},
      "free_svg": true,
      "id": 1,
      "name": "Ava Chen",
      "slug": "string",
      "style": {},
      "tags": [
        {}
      ],
      "thumbnails": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object | Author details. |
| `created` | date | Icon creation timestamp. |
| `family` | object | Icon family details. |
| `free_svg` | boolean | Whether SVG is free. |
| `id` | number | Icon ID. |
| `name` | string | Icon name. |
| `slug` | string | Icon slug. |
| `style` | object | Icon style details. |
| `tags` | array<object> | Icon tags. |
| `thumbnails` | array<object> | Thumbnail images. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/icons` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-icons.md) for the provider-specific parameters and requirements.

