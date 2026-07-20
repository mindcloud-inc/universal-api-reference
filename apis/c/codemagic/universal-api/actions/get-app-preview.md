# Codemagic: Get App Preview

Retrieves a specific app preview from Codemagic.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-app-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-app-preview?connectionId=$CONNECTION_ID&previewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "previewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-app-preview?${params}`, {
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
| `previewId` | string | yes | Codemagic app preview identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app": {},
      "artifact": {},
      "build": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "streaming_public_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | object |  |
| `artifact` | object |  |
| `build` | object |  |
| `created_at` | date |  |
| `deleted_at` | date |  |
| `expires_at` | date |  |
| `id` | string |  |
| `streaming_public_key` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/previews/:preview_id` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-preview.md) for the provider-specific parameters and requirements.

