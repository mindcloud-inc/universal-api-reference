# Airmeet: Create Session

Creates a new session in Airmeet.

```
POST https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/create-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airmeet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "airmeetId": "string",
  "hostEmail": "ava@example.com",
  "sessionDuration": 1,
  "sessionStartTime": 1,
  "sessionTitle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/create-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "airmeetId": "string",
    "hostEmail": "ava@example.com",
    "sessionDuration": 1,
    "sessionStartTime": 1,
    "sessionTitle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `airmeetId` | string | yes | The Airmeet event ID. |
| `hostEmail` | string | yes | Email of the host or community team member running the session. |
| `sessionDuration` | number | yes | Session duration in minutes. |
| `sessionStartTime` | number | yes | Session start time as a Unix timestamp in milliseconds. |
| `sessionTitle` | string | yes | Title of the session. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airmeet API returns.

## Native endpoint

Through the native Airmeet API, this operation is `POST /airmeet/{airmeetId}/session` (base URL `https://api-gateway-prod.us.airmeet.com/prod`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session.md) for the provider-specific parameters and requirements.

