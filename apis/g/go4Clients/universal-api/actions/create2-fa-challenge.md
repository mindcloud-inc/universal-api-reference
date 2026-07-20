# Go4Clients: Create 2FA Challenge

Creates a two-factor authentication challenge in Go4Clients.

```
POST https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create2-fa-challenge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create2-fa-challenge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "application": "MindCloud",
  "key": "57311224477"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/create2-fa-challenge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "application": "MindCloud",
    "key": "57311224477"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `application` | string | yes | Application creating the 2FA challenge. Example: `MindCloud`. |
| `key` | string | yes | Challenge key, typically a phone number. Example: `57311224477`. |
| `validMinutes` | number | no | Expiration time in minutes for the generated code. Example: `10`. |
| `maxAttempts` | number | no | Maximum validation attempts before the code is blocked. Example: `20`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Go4Clients API returns.

## Native endpoint

Through the native Go4Clients API, this operation is `POST /api/tfa/v1.0` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create2-fa-challenge.md) for the provider-specific parameters and requirements.

