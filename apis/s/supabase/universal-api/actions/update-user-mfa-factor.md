# Supabase: Update User MFA Factor



```
PUT https://connect.mindcloud.co/v1/universal/supabase/latest/actions/update-user-mfa-factor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/update-user-mfa-factor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supabase/latest/actions/update-user-mfa-factor', {
  method: 'PUT',
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

Through the native Supabase API, this operation is `PUT /auth/v1/admin/users/:userId/factors/:factorId` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-mfa-factor.md) for the provider-specific parameters and requirements.

