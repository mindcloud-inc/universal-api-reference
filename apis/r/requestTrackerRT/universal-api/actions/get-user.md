# Request Tracker (RT): Get User

Retrieves a user from Request Tracker.

```
GET https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Request Tracker (RT) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-user?${params}`, {
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
| `userId` | string | yes | The RT user ID or username. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled": "string",
      "emailAddress": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "privileged": 1,
      "realName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled` | string |  |
| `emailAddress` | string |  |
| `id` | number |  |
| `name` | string |  |
| `privileged` | number |  |
| `realName` | string |  |

## Native endpoint

Through the native Request Tracker (RT) API, this operation is `GET user/:userId` (base URL `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

