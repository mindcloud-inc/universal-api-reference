# EducateMe: Update User

Updates an existing user in EducateMe.

```
PUT https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Existing user email. Example: `apps@mindcloud.co`. |
| `tagNamesToConnect[]` | array<string> | no | Tag names to connect. Example: `Codex Stage3 Tag 20260331B`. |
| `tagNamesToDisconnect[]` | array<string> | no | Tag names to disconnect. Example: `Codex Stage3 Tag 20260331B`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `newEmail` | string | no | Optional new email to update to. Example: `apps+renamed@mindcloud.co`. |
| `customProperties[]` | array<object> | no | Optional custom properties. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EducateMe API returns.

## Native endpoint

Through the native EducateMe API, this operation is `POST /users/:email` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

