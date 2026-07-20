# Digital Samba: Get bookmarks

Retrieves recording bookmarks from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-bookmarks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-bookmarks?connectionId=$CONNECTION_ID&recording=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recording": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-bookmarks?${params}`, {
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
| `recording` | string | yes | Recording path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookmark": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "participantId": "string",
      "sessionId": "string",
      "time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookmark` | string | Bookmark text. |
| `createdAt` | date | Creation timestamp. |
| `id` | string | Bookmark identifier. |
| `participantId` | string | Participant identifier. |
| `sessionId` | string | Session identifier. |
| `time` | number | Bookmark time offset. |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /recordings/:recording/bookmarks` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bookmarks.md) for the provider-specific parameters and requirements.

