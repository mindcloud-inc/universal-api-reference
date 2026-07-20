# Airtop: Create Session

Creates a new session in Airtop.

```
POST https://connect.mindcloud.co/v1/universal/airtop/latest/actions/create-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airtop/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airtop/latest/actions/create-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `configuration.baseProfileId` | string | no | Base profile ID to clone when creating the session |
| `configuration.persistProfile` | boolean | no | Persist the session profile for later reuse |
| `configuration.timeoutMinutes` | number | no | Maximum session duration in minutes |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airtop API returns.

## Native endpoint

Through the native Airtop API, this operation is `POST /sessions` (base URL `https://api.airtop.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session.md) for the provider-specific parameters and requirements.

