# Digital Samba: Get the specified recording

Retrieves a recording from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-the-specified-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-the-specified-recording?connectionId=$CONNECTION_ID&recording=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recording": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-the-specified-recording?${params}`, {
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
      "createdAt": "string",
      "duration": 1,
      "externalRoomId": "string",
      "friendlyUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "participantExternalId": "string",
      "participantId": "string",
      "participantName": "Ava Chen",
      "privacy": "string",
      "roomId": "string",
      "roomIsDeleted": true,
      "sessionId": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `duration` | number |  |
| `externalRoomId` | string |  |
| `friendlyUrl` | string |  |
| `id` | string |  |
| `name` | string |  |
| `participantExternalId` | string |  |
| `participantId` | string |  |
| `participantName` | string |  |
| `privacy` | string |  |
| `roomId` | string |  |
| `roomIsDeleted` | boolean |  |
| `sessionId` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /recordings/:recording` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-the-specified-recording.md) for the provider-specific parameters and requirements.

