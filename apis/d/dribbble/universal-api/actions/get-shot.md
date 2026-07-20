# Dribbble: Get Shot



```
GET https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-shot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dribbble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-shot?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-shot?${params}`, {
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
| `id` | number | yes | The Dribbble shot ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "animated": true,
      "attachments": [
        {}
      ],
      "description": "string",
      "height": 1,
      "htmlUrl": "https://example.com",
      "id": 1,
      "images": {},
      "lowProfile": true,
      "projects": [
        {}
      ],
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "team": {},
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "video": {},
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `animated` | boolean |  |
| `attachments` | array<object> |  |
| `description` | string |  |
| `height` | number |  |
| `htmlUrl` | string |  |
| `id` | number |  |
| `images` | object |  |
| `lowProfile` | boolean |  |
| `projects` | array<object> |  |
| `publishedAt` | date |  |
| `tags` | array<string> |  |
| `team` | object |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `video` | object |  |
| `width` | number |  |

## Native endpoint

Through the native Dribbble API, this operation is `GET /shots/:id` (base URL `https://api.dribbble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shot.md) for the provider-specific parameters and requirements.

