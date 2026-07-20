# Digital Samba: Get participant statistics

Retrieves participant statistics from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-participant-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-participant-statistics?connectionId=$CONNECTION_ID&participant=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "participant": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-participant-statistics?${params}`, {
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
| `participant` | string | yes | Participant path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": 1,
      "browser": "string",
      "device": "string",
      "e2ee": true,
      "joinTime": "string",
      "leaveTime": "string",
      "live": true,
      "participantName": "Ava Chen",
      "participationMinutes": 1,
      "publicChatPosts": 1,
      "questions": 1,
      "role": "string",
      "roomExternalId": "string",
      "roomFriendlyUrl": "https://example.com",
      "roomId": "string",
      "roomIsDeleted": true,
      "roomPrivacy": "string",
      "sessionId": "string",
      "system": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | number |  |
| `browser` | string |  |
| `device` | string |  |
| `e2ee` | boolean |  |
| `joinTime` | string |  |
| `leaveTime` | string |  |
| `live` | boolean |  |
| `participantName` | string |  |
| `participationMinutes` | number |  |
| `publicChatPosts` | number |  |
| `questions` | number |  |
| `role` | string |  |
| `roomExternalId` | string |  |
| `roomFriendlyUrl` | string |  |
| `roomId` | string |  |
| `roomIsDeleted` | boolean |  |
| `roomPrivacy` | string |  |
| `sessionId` | string |  |
| `system` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /participants/:participant` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-participant-statistics.md) for the provider-specific parameters and requirements.

