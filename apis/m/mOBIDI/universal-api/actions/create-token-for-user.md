# MOBIDI: Create Token For User

Creates a user access token in MOBIDI.

```
POST https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-token-for-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-token-for-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "Ava Chen",
  "password": "string",
  "tokenTarget": "Any"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/create-token-for-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "Ava Chen",
    "password": "string",
    "tokenTarget": "Any"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | MOBIDI username to mint a token for. |
| `password` | string | yes | MOBIDI password paired with the username. |
| `tokenTarget` | string | yes | Target scope for the generated token. Default: `Any`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MOBIDI API returns.

## Native endpoint

Through the native MOBIDI API, this operation is `GET /MobidiTokenHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-token-for-user.md) for the provider-specific parameters and requirements.

