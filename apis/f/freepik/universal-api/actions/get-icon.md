# Freepik: Get Icon

Retrieves detailed icon information from Freepik.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-icon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-icon?connectionId=$CONNECTION_ID&id=4326138" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "4326138"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/get-icon?${params}`, {
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
| `id` | number | yes | Freepik icon identifier. Default: `4326138`. |

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
      "related": {},
      "slug": "string",
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
| `related` | object | Related icons. |
| `slug` | string | Icon slug. |
| `tags` | array<object> | Icon tags. |
| `thumbnails` | array<object> | Thumbnail images. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/icons/{{id}}` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-icon.md) for the provider-specific parameters and requirements.

