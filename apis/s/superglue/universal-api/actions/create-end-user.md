# Superglue: Create End User



```
POST https://connect.mindcloud.co/v1/universal/superglue/latest/actions/create-end-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superglue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superglue/latest/actions/create-end-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superglue/latest/actions/create-end-user', {
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
| `externalId` | string | no | Your application's user ID. Auto-generated if omitted. Example: `user-123`. |
| `email` | string | no | End user's email address. Example: `user@example.com`. |
| `name` | string | no | End user's display name. Example: `John Doe`. |
| `allowedSystems[]` | array<string> | no | Array of system IDs, or ["*"] for all systems. Defaults to no access. Example: `*`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedSystems": [
        "string"
      ],
      "apiKey": "string",
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
| `apiKey` | string | End-user API key returned only when the end user is created. |
| `createdAt` | date | End user creation timestamp. |
| `email` | string | End user email address. |
| `externalId` | string | Application-defined external user ID. |
| `id` | string | Internal Superglue end user ID. |
| `metadata` | object | Custom metadata for the end user. |
| `name` | string | End user display name. |
| `updatedAt` | date | End user update timestamp. |

## Native endpoint

Through the native Superglue API, this operation is `POST /end-users` (base URL `https://api.superglue.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-end-user.md) for the provider-specific parameters and requirements.

