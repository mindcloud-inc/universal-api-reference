# SeekTable: Create User Account

Creates a new user account in SeekTable.

```
POST https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/create-user-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/create-user-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "codex.seektable.stage3+create@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/create-user-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "codex.seektable.stage3+create@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Login email for the new SeekTable account. Example: `codex.seektable.stage3+create@example.com`. |
| `name` | string | no | Example: `Codex Stage 3 Test User`. |
| `teamSharing` | boolean | no | Enable only when the SeekTable installation includes the Team sharing capability. |
| `advancedPublishing` | boolean | no | Enable only when the SeekTable installation includes the Advanced publishing capability. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `POST /api/account` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-account.md) for the provider-specific parameters and requirements.

