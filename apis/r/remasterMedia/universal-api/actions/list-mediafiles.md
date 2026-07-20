# RemasterMedia: List Mediafiles

Retrieves mediafiles from RemasterMedia.

```
GET https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/list-mediafiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemasterMedia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/list-mediafiles?connectionId=$CONNECTION_ID&from=2026-04-19T00%3A00%3A00Z&to=2026-04-20T23%3A59%3A59Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-19T00:00:00Z",
  "to": "2026-04-20T23:59:59Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/list-mediafiles?${params}`, {
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
| `from` | date | yes | Beginning of time range as RFC3339. Default: `2026-04-19T00:00:00Z`. |
| `to` | date | yes | End of time range as RFC3339. Default: `2026-04-20T23:59:59Z`. |
| `page` | number | no | Page number. Defaults to 1. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mediafiles": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mediafiles` | array<object> | Mediafiles in the requested time range. |
| `mediafiles[].action` | string |  |
| `mediafiles[].created_at` | date |  |
| `mediafiles[].expires_at` | date |  |
| `mediafiles[].id` | string |  |
| `mediafiles[].metadata` | object |  |
| `mediafiles[].options` | object |  |
| `mediafiles[].status` | string |  |
| `mediafiles[].updated_at` | date |  |
| `mediafiles[].url` | string |  |
| `mediafiles[].user_data` | object |  |
| `mediafiles[].webhook_url` | string |  |

## Native endpoint

Through the native RemasterMedia API, this operation is `GET /mediafiles` (base URL `https://api-sandbox.remastermedia.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mediafiles.md) for the provider-specific parameters and requirements.

