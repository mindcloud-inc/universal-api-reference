# Codemagic: Get Shared App Preview

Retrieves a shared app preview from Codemagic.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-shared-app-preview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-shared-app-preview?connectionId=$CONNECTION_ID&sharedPreviewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sharedPreviewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-shared-app-preview?${params}`, {
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
| `sharedPreviewId` | string | yes | Codemagic shared preview identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `expires_at` | date |  |
| `id` | string |  |
| `streaming_public_key` | string |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/shared-previews/:shared_preview_id` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shared-app-preview.md) for the provider-specific parameters and requirements.

