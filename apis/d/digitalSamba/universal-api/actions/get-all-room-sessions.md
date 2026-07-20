# Digital Samba: Get all room sessions

Retrieves room sessions from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-room-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-room-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0&room=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "room": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-room-sessions?${params}`, {
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
| `room` | string | yes | Room path parameter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateStart` | string | no | Period start date. Must be a valid date in the format Y-m-d. |
| `dateEnd` | string | no | Period end date. Must be a valid date in the format Y-m-d. |
| `after` | string | no | The UUID of the room or room friendly URL after which records will be returned. |
| `live` | boolean | no | Flag to filter live or archive sessions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "endTime": "string",
      "friendlyUrl": "https://example.com",
      "id": "string",
      "live": true,
      "participantsLive": 1,
      "participantsMax": 1,
      "participantsTotal": 1,
      "roomExternalId": "string",
      "roomId": "string",
      "roomIsDeleted": true,
      "startTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `endTime` | string |  |
| `friendlyUrl` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `participantsLive` | number |  |
| `participantsMax` | number |  |
| `participantsTotal` | number |  |
| `roomExternalId` | string |  |
| `roomId` | string |  |
| `roomIsDeleted` | boolean |  |
| `startTime` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /rooms/:room/sessions` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-room-sessions.md) for the provider-specific parameters and requirements.

