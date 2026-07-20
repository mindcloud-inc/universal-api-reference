# Vimeo: Get Showcase

Retrieves a showcase record from Vimeo.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-showcase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-showcase?connectionId=$CONNECTION_ID&userId=152184&albumId=40988" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "152184",
  "albumId": "40988"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-showcase?${params}`, {
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
| `userId` | number | yes | The ID of the user. Example: `152184`. |
| `albumId` | number | yes | The ID of the showcase. Example: `40988`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "layout": "string",
      "link": "https://example.com",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "shareLink": "https://example.com",
      "sort": "string",
      "theme": "string",
      "totalClips": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date | When the showcase was created. |
| `description` | string | The showcase description. |
| `duration` | number | Total showcase duration in seconds. |
| `layout` | string | The showcase layout mode. |
| `link` | string | The public Vimeo showcase URL. |
| `modifiedTime` | date | When the showcase was last modified. |
| `name` | string | The showcase name. |
| `shareLink` | string | The share link for the showcase. |
| `sort` | string | The showcase sort mode. |
| `theme` | string | The showcase theme. |
| `totalClips` | number | Total number of clips in the showcase. |
| `uri` | string | The showcase API URI. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /users/:user_id/albums/:album_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-showcase.md) for the provider-specific parameters and requirements.

