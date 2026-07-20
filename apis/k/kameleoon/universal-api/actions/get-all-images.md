# Kameleoon: Get all images



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-images?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-images?${params}`, {
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
| `paramsIo` | string | yes | Required query object documented by Kameleoon for list endpoints. Example: `page=1, perPage=20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altText": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "format": "string",
      "height": 1,
      "id": 1,
      "keywords": [
        "string"
      ],
      "name": "Ava Chen",
      "path": "string",
      "shared": true,
      "siteId": 1,
      "size": 1,
      "sourceUrl": "https://example.com",
      "tags": [
        "string"
      ],
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altText` | string |  |
| `date` | date |  |
| `description` | string |  |
| `format` | string |  |
| `height` | number |  |
| `id` | number |  |
| `keywords` | array<string> |  |
| `name` | string |  |
| `path` | string |  |
| `shared` | boolean |  |
| `siteId` | number |  |
| `size` | number |  |
| `sourceUrl` | string |  |
| `tags` | array<string> |  |
| `width` | number |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET images` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-images.md) for the provider-specific parameters and requirements.

