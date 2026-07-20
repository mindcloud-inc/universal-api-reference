# Stormboard: List Storm Participants

Retrieves participants from a Storm in Stormboard.

```
GET https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storm-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storm-participants?connectionId=$CONNECTION_ID&stormId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stormId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/list-storm-participants?${params}`, {
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
| `stormId` | number | yes | Storm ID from the Stormboard share dialog or related storm record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "users": [
        {
          "comments": 1,
          "email": "ava@example.com",
          "firstname": "Ava",
          "id": 1,
          "ideas": 1,
          "lastactivity": "string",
          "lastname": "Chen",
          "username": "Ava Chen",
          "votes": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `users` | array<object> |  |
| `users[].comments` | number |  |
| `users[].email` | string |  |
| `users[].firstname` | string |  |
| `users[].id` | number |  |
| `users[].ideas` | number |  |
| `users[].lastactivity` | string |  |
| `users[].lastname` | string |  |
| `users[].username` | string |  |
| `users[].votes` | number |  |

## Native endpoint

Through the native Stormboard API, this operation is `GET /storms/:storm_id/users` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-storm-participants.md) for the provider-specific parameters and requirements.

