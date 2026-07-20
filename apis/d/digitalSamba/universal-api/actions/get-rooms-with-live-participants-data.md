# Digital Samba: Get rooms with live participants data

Retrieves live participant data for rooms in Digital Samba.

```
GET https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-rooms-with-live-participants-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digital Samba `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-rooms-with-live-participants-data?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-rooms-with-live-participants-data?${params}`, {
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
| `after` | string | no | The UUID of the room or room friendly URL after which records will be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalId": "string",
      "id": "string",
      "liveParticipants": [
        {}
      ],
      "sessionDuration": 1,
      "startTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalId` | string |  |
| `id` | string |  |
| `liveParticipants` | array<object> |  |
| `sessionDuration` | number |  |
| `startTime` | string |  |

## Native endpoint

Through the native Digital Samba API, this operation is `GET /rooms/live/participants` (base URL `https://api.digitalsamba.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-rooms-with-live-participants-data.md) for the provider-specific parameters and requirements.

