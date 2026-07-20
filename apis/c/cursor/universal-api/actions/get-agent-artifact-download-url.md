# Cursor: Get Agent Artifact Download URL



```
GET https://connect.mindcloud.co/v1/universal/cursor/latest/actions/get-agent-artifact-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/get-agent-artifact-download-url?connectionId=$CONNECTION_ID&id=bc_abc123&path=%2Fopt%2Fcursor%2Fartifacts%2Fscreenshot.png" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "bc_abc123",
  "path": "/opt/cursor/artifacts/screenshot.png"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursor/latest/actions/get-agent-artifact-download-url?${params}`, {
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
| `id` | string | yes | Unique identifier for the cloud agent that produced the artifact. Example: `bc_abc123`. |
| `path` | string | yes | Absolute artifact path returned by List Agent Artifacts, for example `/opt/cursor/artifacts/screenshot.png`. Example: `/opt/cursor/artifacts/screenshot.png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | date | Expiration time for the presigned download URL. |
| `url` | string | Temporary presigned S3 download URL. |

## Native endpoint

Through the native Cursor API, this operation is `GET /v0/agents/{{id}}/artifacts/download` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-artifact-download-url.md) for the provider-specific parameters and requirements.

