# Superglue: Update End User



```
PUT https://connect.mindcloud.co/v1/universal/superglue/latest/actions/update-end-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/update-end-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endUserId": "550e8400-e29b-41d4-a716-446655440000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superglue/latest/actions/update-end-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endUserId": "550e8400-e29b-41d4-a716-446655440000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endUserId` | string | yes | Internal Superglue end-user ID. Example: `550e8400-e29b-41d4-a716-446655440000`. |
| `externalId` | string | no | Your application's user ID. Example: `user-123`. |
| `email` | string | no | End user's email address. Example: `user@example.com`. |
| `name` | string | no | End user's display name. Example: `John Doe`. |
| `allowedSystems[]` | array<string> | no | Array of system IDs, or ["*"] for all systems. Example: `*`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedSystems": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedSystems` | array<string> | System IDs this user can access. |
| `createdAt` | date | End user creation timestamp. |
| `email` | string | End user email address. |
| `externalId` | string | Application-defined external user ID. |
| `id` | string | Internal Superglue end user ID. |
| `metadata` | object | Custom metadata for the end user. |
| `name` | string | End user display name. |
| `updatedAt` | date | End user update timestamp. |

## Native endpoint

Through the native Superglue API, this operation is `PATCH /end-users/:endUserId` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-end-user.md) for the provider-specific parameters and requirements.

