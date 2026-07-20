# Teletype App: List Dialogs

Retrieves all dialogs from Teletype App.

```
GET https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/list-dialogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teletype App `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/list-dialogs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/list-dialogs?${params}`, {
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
      "countNewMessages": 1,
      "createdAt": {},
      "id": "string",
      "isUnanswered": true,
      "lastMessage": {},
      "lastSessionId": "string",
      "seen": true,
      "status": 1,
      "statusName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countNewMessages` | number |  |
| `createdAt` | object |  |
| `id` | string |  |
| `isUnanswered` | boolean |  |
| `lastMessage` | object |  |
| `lastSessionId` | string |  |
| `seen` | boolean |  |
| `status` | number |  |
| `statusName` | string |  |

## Native endpoint

Through the native Teletype App API, this operation is `GET /dialogs` (base URL `https://api.teletype.app/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-dialogs.md) for the provider-specific parameters and requirements.

