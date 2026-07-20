# Documo: Create API Key

Creates a new API key in Documo.

```
POST https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "access": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-api-key', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "access": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `access` | string | yes | String \| Required \| Possible values: admin, base, print_driver |
| `name` | string | no | String \| 128 characters limit \| Key name \| Default: null |
| `userId` | string | no | Uuid \| User id that will be assigned to key \| Default: current user |
| `expiresAt` | string | no | String \| Expire date |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deviceId": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "token": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {
        "email": "ava@example.com",
        "uuid": "string"
      },
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `createdAt` | date |  |
| `deviceId` | string |  |
| `expiresAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `token` | string |  |
| `updatedAt` | date |  |
| `user.email` | string |  |
| `user.uuid` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Documo API, this operation is `POST /api-keys` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-api-key.md) for the provider-specific parameters and requirements.

