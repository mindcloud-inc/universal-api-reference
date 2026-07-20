# Livestorm: List Session Recordings

Retrieves recordings for a session from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-session-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-session-recordings?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-session-recordings?${params}`, {
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
| `id` | string | yes | Session ID |
| `urlExpiresIn` | number | no | Custom expiry time for signed URLs in seconds (1 hour to 7 days). Defaults to 12 hours (43200 seconds) if not provided. Must be a single integer value (e.g., `?url_expires_in=604800`), not a nested parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "eventId": "string",
        "fileName": "Ava Chen",
        "fileSize": 1,
        "fileType": "string",
        "mimeType": "string",
        "sessionId": "string",
        "url": "https://example.com",
        "urlExpiresIn": 1,
        "urlGeneratedAt": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.eventId` | string |  |
| `attributes.fileName` | string |  |
| `attributes.fileSize` | number |  |
| `attributes.fileType` | string |  |
| `attributes.mimeType` | string |  |
| `attributes.sessionId` | string |  |
| `attributes.url` | string |  |
| `attributes.urlExpiresIn` | number |  |
| `attributes.urlGeneratedAt` | number |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `GET sessions/:id/recordings` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-session-recordings.md) for the provider-specific parameters and requirements.

