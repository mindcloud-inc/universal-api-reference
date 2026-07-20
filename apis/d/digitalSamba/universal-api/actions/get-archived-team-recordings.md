# Digital Samba: Get archived team recordings

Retrieves archived team recordings from Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-archived-team-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-archived-team-recordings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-archived-team-recordings?${params}`, {
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
| `roomId` | string | no | The UUID of the room. |
| `after` | string | no | The UUID of the recording after which records will be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "externalRoomId": "string",
      "friendlyUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "participantExternalId": "string",
      "participantId": "string",
      "participantName": "Ava Chen",
      "privacy": "string",
      "roomId": "string",
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
| `externalRoomId` | string |  |
| `friendlyUrl` | string |  |
| `id` | string |  |
| `name` | string |  |
| `participantExternalId` | string |  |
| `participantId` | string |  |
| `participantName` | string |  |
| `privacy` | string |  |
| `roomId` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /recordings/archived` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-archived-team-recordings.md) for the provider-specific parameters and requirements.

