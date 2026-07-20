# Tailwind: List Accounts

Retrieves Pinterest accounts from Tailwind.

```
GET https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tailwind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "id": "string",
      "isDomainVerified": true,
      "tokenAuthorized": true,
      "userId": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string | Profile image URL. |
| `createdAt` | date | When the account was connected. |
| `displayName` | string | Display name. |
| `id` | string | Tailwind account ID. |
| `isDomainVerified` | boolean | Whether the account domain is verified. |
| `tokenAuthorized` | boolean | Whether the Pinterest token is valid. |
| `userId` | string | Pinterest user ID. |
| `username` | string | Pinterest username. |

## Native endpoint

Through the native Tailwind API, this operation is `GET /v1/accounts` (base URL `https://api-v1.tailwind.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

