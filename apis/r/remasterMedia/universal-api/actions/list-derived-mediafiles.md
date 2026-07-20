# RemasterMedia: List Derived Mediafiles

Retrieves derived mediafiles from RemasterMedia.

```
GET https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/list-derived-mediafiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemasterMedia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/list-derived-mediafiles?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/list-derived-mediafiles?${params}`, {
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
| `id` | string | yes | ID of the mediafile whose derived mediafiles should be listed. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `created_at` | date |  |
| `expires_at` | date |  |
| `id` | string |  |
| `metadata` | object |  |
| `options` | object |  |
| `status` | string |  |
| `updated_at` | date |  |
| `url` | string |  |
| `user_data` | object |  |
| `webhook_url` | string |  |

## Native endpoint

Through the native RemasterMedia API, this operation is `GET /mediafile/{{id}}/derived` (base URL `https://api-sandbox.remastermedia.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-derived-mediafiles.md) for the provider-specific parameters and requirements.

