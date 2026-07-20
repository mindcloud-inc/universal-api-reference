# Assembly.com: List Clients

Retrieves clients from Assembly.com.

```
GET https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-clients?${params}`, {
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
| `companyId` | string | no | Any of the company IDs of the client user(s) to query for. |
| `email` | string | no | The email of the client user to query for (exact match, case-sensitive). |
| `familyName` | string | no | The family name of the client user(s) to query for (exact match, case-sensitive). |
| `givenName` | string | no | The given name of the client user(s) to query for (exact match, case-sensitive). |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].avatarImageUrl` | string |  |
| `data[].companyId` | string |  |
| `data[].companyIds[]` | string |  |
| `data[].createdAt` | date |  |
| `data[].creationMethod` | string |  |
| `data[].email` | string |  |
| `data[].fallbackColor` | string |  |
| `data[].familyName` | string |  |
| `data[].firstLoginDate` | object |  |
| `data[].givenName` | string |  |
| `data[].id` | string |  |
| `data[].invitedBy` | string |  |
| `data[].inviteUrl` | string |  |
| `data[].lastLoginDate` | object |  |
| `data[].object` | string |  |
| `data[].openDeepLinksInDesktopApp` | object |  |
| `data[].status` | string |  |
| `data[].updatedAt` | date |  |

## Native endpoint

Through the native Assembly.com API, this operation is `GET /clients` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

