# Daytona: Create Sandbox SSH Access

Creates sandbox SSH access in Daytona.

```
POST https://connect.mindcloud.co/v1/universal/daytona/latest/actions/create-sandbox-ssh-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/create-sandbox-ssh-access" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sandboxIdOrName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/daytona/latest/actions/create-sandbox-ssh-access', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sandboxIdOrName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sandboxIdOrName` | string | yes | ID or name of the sandbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "sandboxId": "string",
      "sshCommand": "string",
      "token": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the SSH access was created. |
| `expiresAt` | date | When the SSH access expires. |
| `id` | string | Unique identifier for the SSH access. |
| `sandboxId` | string | ID of the sandbox this SSH access is for. |
| `sshCommand` | string | SSH command to connect to the sandbox. |
| `token` | string | SSH access token. |
| `updatedAt` | date | When the SSH access was last updated. |

## Native endpoint

Through the native Daytona API, this operation is `POST /sandbox/[:sandboxIdOrName]/ssh-access` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sandbox-ssh-access.md) for the provider-specific parameters and requirements.

