# Timetonic: User Login

Creates an OAuth key in Timetonic for user login.

```
POST https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/user-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/user-login" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "login": "apps@mindcloud.co",
  "password": "Real TimeTonic password required",
  "appkey": "Paste appkey from Register Application"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/user-login', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "login": "apps@mindcloud.co",
    "password": "Real TimeTonic password required",
    "appkey": "Paste appkey from Register Application"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `login` | string | yes | TimeTonic login username or email. Example: `apps@mindcloud.co`. |
| `password` | string | yes | TimeTonic account password. Example: `Real TimeTonic password required`. |
| `appkey` | string | yes | App key returned by Register Application. Example: `Paste appkey from Register Application`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Timetonic API returns.

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/user-login.md) for the provider-specific parameters and requirements.

