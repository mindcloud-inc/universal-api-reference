# SeekTable: Update User Account

Updates an existing user account in SeekTable.

```
PUT https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/update-user-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/update-user-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/update-user-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the user account to update. Example: `1`. |
| `email` | string | no | New login email for the user account. Example: `codex.seektable.stage3+updated@example.com`. |
| `name` | string | no | Example: `Codex Stage 3 Updated User`. |
| `teamSharing` | boolean | no | Enable only when the SeekTable installation includes the Team sharing capability. |
| `advancedPublishing` | boolean | no | Enable only when the SeekTable installation includes the Advanced publishing capability. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `PUT /api/account/:id` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-account.md) for the provider-specific parameters and requirements.

