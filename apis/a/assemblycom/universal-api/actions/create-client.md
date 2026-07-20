# Assembly.com: Create Client

Creates a client in Assembly.com.

```
POST https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "givenName": "Ava Chen",
  "familyName": "Ava Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "givenName": "Ava Chen",
    "familyName": "Ava Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendInvite` | boolean | no | If true then send an account invite to the client. Default: `false`. |
| `givenName` | string | yes |  |
| `familyName` | string | yes |  |
| `email` | string | yes |  |
| `companyId` | string | no | The ID of the company this client belongs to. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields` | object | no | Optional custom field map keyed by Assembly custom field keys. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarImageUrl": "https://example.com",
      "companyId": "string",
      "companyIds": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creationMethod": "string",
      "email": "ava@example.com",
      "fallbackColor": "string",
      "familyName": "Ava Chen",
      "firstLoginDate": {},
      "givenName": "Ava Chen",
      "id": "string",
      "invitedBy": "string",
      "inviteUrl": "https://example.com",
      "lastLoginDate": {},
      "object": "string",
      "openDeepLinksInDesktopApp": {},
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarImageUrl` | string |  |
| `companyId` | string |  |
| `companyIds[]` | string |  |
| `createdAt` | date |  |
| `creationMethod` | string |  |
| `email` | string |  |
| `fallbackColor` | string |  |
| `familyName` | string |  |
| `firstLoginDate` | object |  |
| `givenName` | string |  |
| `id` | string |  |
| `invitedBy` | string |  |
| `inviteUrl` | string |  |
| `lastLoginDate` | object |  |
| `object` | string |  |
| `openDeepLinksInDesktopApp` | object |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Assembly.com API, this operation is `POST /clients` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

