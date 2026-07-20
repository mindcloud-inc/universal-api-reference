# Everhour: List User Time Records

Retrieves time records for a user from Everhour.

```
GET https://connect.mindcloud.co/v1/universal/everhour/latest/actions/list-user-time-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/list-user-time-records?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everhour/latest/actions/list-user-time-records?${params}`, {
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
| `from` | string | no | Start date for the time range. |
| `limit` | number | no | Maximum number of records to return. |
| `page` | number | no | Page number to return. |
| `to` | string | no | End date for the time range. |
| `userId` | string | yes | Everhour user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isInvoiced": true,
      "isLocked": true,
      "task": {},
      "time": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `date` | date |  |
| `id` | number |  |
| `isInvoiced` | boolean |  |
| `isLocked` | boolean |  |
| `task` | object |  |
| `time` | number |  |
| `user` | number |  |

## Native endpoint

Through the native Everhour API, this operation is `GET /users/:userId/time` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-time-records.md) for the provider-specific parameters and requirements.

