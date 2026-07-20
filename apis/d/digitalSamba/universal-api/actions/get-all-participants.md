# Digital Samba: Get all participants

Retrieves participants from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-participants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-participants?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dateStart` | string | no | Period start date. Must be a valid date in the format Y-m-d. |
| `dateEnd` | string | no | Period end date. Must be a valid date in the format Y-m-d. |
| `after` | string | no | The UUID of the room or room friendly URL after which records will be returned. |
| `live` | boolean | no | Flag to filter live or archive sessions. |
| `roomId` | string | no | The UUID of the room to filter session by specific room. |
| `sessionId` | string | no | The UUID of the session to filter participants by specific session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalId": "string",
      "friendlyUrl": "https://example.com",
      "id": "string",
      "joinTime": "string",
      "leaveTime": "string",
      "live": true,
      "name": "Ava Chen",
      "role": "string",
      "roomExternalId": "string",
      "roomId": "string",
      "roomIsDeleted": true,
      "sessionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalId` | string |  |
| `friendlyUrl` | string |  |
| `id` | string |  |
| `joinTime` | string |  |
| `leaveTime` | string |  |
| `live` | boolean |  |
| `name` | string |  |
| `role` | string |  |
| `roomExternalId` | string |  |
| `roomId` | string |  |
| `roomIsDeleted` | boolean |  |
| `sessionId` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /participants` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-participants.md) for the provider-specific parameters and requirements.

