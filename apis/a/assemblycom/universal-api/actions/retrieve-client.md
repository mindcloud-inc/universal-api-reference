# Assembly.com: Retrieve Client

Retrieves a client from Assembly.com by ID.

```
GET https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/retrieve-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/retrieve-client?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/retrieve-client?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique ID of the client to retrieve |

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
      "customFields": {},
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
| `customFields` | object |  |
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

Through the native Assembly.com API, this operation is `GET /clients/:id` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-client.md) for the provider-specific parameters and requirements.

