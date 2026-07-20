# Supabase: List User MFA Factors

Retrieves a user's MFA factors from Supabase Auth.

```
GET https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-user-mfa-factors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-user-mfa-factors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-user-mfa-factors?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "factorType": "string",
      "friendlyName": "Ava Chen",
      "id": "string",
      "lastChallengedAt": "2026-05-07T12:00:00.000Z",
      "phone": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webauthnCredential": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `factorType` | string |  |
| `friendlyName` | string |  |
| `id` | string |  |
| `lastChallengedAt` | date |  |
| `phone` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `webauthnCredential` | string |  |

## Native endpoint

Through the native Supabase API, this operation is `GET /auth/v1/admin/users/:userId/factors` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-mfa-factors.md) for the provider-specific parameters and requirements.

