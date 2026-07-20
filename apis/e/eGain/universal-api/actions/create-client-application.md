# eGain: Create Client Application

Creates a new client application in eGain.

```
POST https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-client-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-client-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": true,
  "name": "Ava Chen",
  "roles[0].callback": "string",
  "roles[0].name": "Ava Chen",
  "roles[0].notificationEmail": "ava@example.com",
  "roles[0].version": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGain/latest/actions/create-client-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active": true,
    "name": "Ava Chen",
    "roles[0].callback": "string",
    "roles[0].name": "Ava Chen",
    "roles[0].notificationEmail": "ava@example.com",
    "roles[0].version": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | yes | Whether the client application is active. |
| `description` | string | no | Client application description. |
| `name` | string | yes | Client application name. |
| `roles[0].callback` | string | yes | Role callback URL. |
| `roles[0].name` | string | yes | Role name. |
| `roles[0].notificationEmail` | string | yes | Role notification email. |
| `roles[0].version` | string | yes | Role version. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eGain API returns.

## Native endpoint

Through the native eGain API, this operation is `POST /clientapplications` (base URL `https://api.ai.egain.cloud/conversation/conversationmgr/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-application.md) for the provider-specific parameters and requirements.

