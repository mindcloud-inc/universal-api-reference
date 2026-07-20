# Frontegg: Update User

Updates an existing user in Frontegg.

```
PUT https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The user ID to update. |
| `name` | string | no | Updated user name. |
| `phoneNumber` | string | no | Updated user phone number in E.164 format. |
| `profilePictureUrl` | string | no | Updated profile picture URL. |
| `metadata` | string | no | Stringified JSON metadata. |
| `vendorMetadata` | string | no | Stringified JSON vendor metadata. |
| `mfaBypass` | boolean | no | Whether MFA should be bypassed for the user. |
| `externalId` | string | no | External identifier for the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalId": "string",
      "id": "string",
      "isLocked": true,
      "metadata": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "provider": "string",
      "tenantId": "string",
      "tenantIds": [
        "string"
      ],
      "vendorMetadata": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `metadata` | string |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `provider` | string |  |
| `tenantId` | string |  |
| `tenantIds` | array<string> |  |
| `vendorMetadata` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Frontegg API, this operation is `PUT /identity/resources/users/v1/:userId` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

