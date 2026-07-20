# Knack: Create Remote User Login



```
POST https://connect.mindcloud.co/v1/universal/knack/latest/actions/create-remote-user-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Knack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/knack/latest/actions/create-remote-user-login" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knack/latest/actions/create-remote-user-login', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address for a non-SSO Knack user account. |
| `password` | string | yes | Password for the non-SSO Knack user account. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Knack API returns.

## Native endpoint

Through the native Knack API, this operation is `POST /applications/{{credentials.applicationId}}/session` (base URL `https://api.knack.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-remote-user-login.md) for the provider-specific parameters and requirements.

