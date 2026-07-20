# Resend: List Broadcasts

Retrieves broadcasts from Resend.

```
GET https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-broadcasts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-broadcasts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/list-broadcasts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "audienceId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "segmentId": "string",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "topicId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audienceId` | string | Deprecated audience identifier returned by Resend. |
| `createdAt` | date | When the broadcast was created. |
| `id` | string | Broadcast identifier. |
| `scheduledAt` | date | Scheduled send time, when present. |
| `segmentId` | string | Segment identifier for the broadcast. |
| `sentAt` | date | Time the broadcast was sent, when present. |
| `status` | string | Broadcast delivery status. |
| `topicId` | string | Associated topic identifier, when present. |

## Native endpoint

Through the native Resend API, this operation is `GET /broadcasts` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-broadcasts.md) for the provider-specific parameters and requirements.

