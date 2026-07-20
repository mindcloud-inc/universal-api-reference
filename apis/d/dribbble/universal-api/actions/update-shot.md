# Dribbble: Update Shot



```
PUT https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/update-shot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dribbble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/update-shot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/update-shot', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Dribbble shot ID. |
| `title` | string | no |  |
| `description` | string | no |  |
| `lowProfile` | boolean | no |  |
| `scheduledFor` | date | no |  |
| `tags[]` | array<string> | no |  |
| `teamId` | number | no |  |

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

Through the native Dribbble API, this operation is `PUT /shots/:id` (base URL `https://api.dribbble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shot.md) for the provider-specific parameters and requirements.

