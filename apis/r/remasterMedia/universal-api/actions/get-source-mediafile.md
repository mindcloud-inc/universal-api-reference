# RemasterMedia: Get Source Mediafile

Retrieves the source mediafile from RemasterMedia.

```
GET https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/get-source-mediafile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemasterMedia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/get-source-mediafile?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/get-source-mediafile?${params}`, {
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
| `id` | string | yes | ID of the mediafile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mediafile": {
        "action": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "expires_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "metadata": {},
        "options": {},
        "status": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com",
        "user_data": {},
        "webhook_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mediafile` | object |  |
| `mediafile.action` | string |  |
| `mediafile.created_at` | date |  |
| `mediafile.expires_at` | date |  |
| `mediafile.id` | string |  |
| `mediafile.metadata` | object |  |
| `mediafile.options` | object |  |
| `mediafile.status` | string |  |
| `mediafile.updated_at` | date |  |
| `mediafile.url` | string |  |
| `mediafile.user_data` | object |  |
| `mediafile.webhook_url` | string |  |

## Native endpoint

Through the native RemasterMedia API, this operation is `GET /mediafile/{{id}}/source` (base URL `https://api-sandbox.remastermedia.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-source-mediafile.md) for the provider-specific parameters and requirements.

