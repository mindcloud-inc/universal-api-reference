# Teletype App: List Clients

Retrieves all clients from Teletype App.

```
GET https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teletype App `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/list-clients?${params}`, {
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
      "averageRate": 1,
      "banned": true,
      "emailIsLocked": true,
      "id": "string",
      "isOnline": true,
      "lastOnlineAt": "2026-05-07T12:00:00.000Z",
      "phoneIsLocked": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageRate` | number |  |
| `banned` | boolean |  |
| `emailIsLocked` | boolean |  |
| `id` | string |  |
| `isOnline` | boolean |  |
| `lastOnlineAt` | date |  |
| `phoneIsLocked` | boolean |  |

## Native endpoint

Through the native Teletype App API, this operation is `GET /clients` (base URL `https://api.teletype.app/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

