# Timetonic: Create Session Key

Creates a session key in Timetonic.

```
POST https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-session-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-session-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "oauthUserId": "OAuth user id from User Login",
  "userId": "TimeTonic user id",
  "oauthkey": "OAuth key from User Login"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/create-session-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "oauthUserId": "OAuth user id from User Login",
    "userId": "TimeTonic user id",
    "oauthkey": "OAuth key from User Login"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `oauthUserId` | string | yes | OAuth user ID returned by User Login. Example: `OAuth user id from User Login`. |
| `userId` | string | yes | TimeTonic user ID for the session. Example: `TimeTonic user id`. |
| `oauthkey` | string | yes | OAuth key returned by User Login. Example: `OAuth key from User Login`. |
| `restrictions` | string | no | Optional session restrictions string. Example: `Optional restrictions`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Timetonic API returns.

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session-key.md) for the provider-specific parameters and requirements.

