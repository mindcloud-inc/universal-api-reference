# Digital Samba: Get session transcripts

Retrieves session transcripts from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-session-transcripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-session-transcripts?connectionId=$CONNECTION_ID&limit=25&offset=0&session=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "session": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-session-transcripts?${params}`, {
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
| `session` | string | yes | Session path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endTime": "string",
      "participantId": "string",
      "participantName": "Ava Chen",
      "startTime": "string",
      "transcript": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endTime` | string |  |
| `participantId` | string |  |
| `participantName` | string |  |
| `startTime` | string |  |
| `transcript` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /sessions/:session/transcripts` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-session-transcripts.md) for the provider-specific parameters and requirements.

