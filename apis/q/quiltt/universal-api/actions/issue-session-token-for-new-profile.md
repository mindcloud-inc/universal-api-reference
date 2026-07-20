# Quiltt: Issue Session Token For New Profile



```
POST https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/issue-session-token-for-new-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quiltt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/issue-session-token-for-new-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/issue-session-token-for-new-profile', {
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
| `email` | string | no | New profile email address. |
| `name` | string | no | New profile display name. |
| `uuid` | string | no | Optional custom UUID for the new profile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "environmentId": "string",
      "expiration": 1,
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "token": "string",
      "userId": "string",
      "userUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environmentId` | string |  |
| `expiration` | number |  |
| `expiresAt` | date |  |
| `token` | string |  |
| `userId` | string |  |
| `userUuid` | string |  |

## Native endpoint

Through the native Quiltt API, this operation is `POST https://auth.quiltt.io/v1/users/sessions` (base URL `https://api.quiltt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-session-token-for-new-profile.md) for the provider-specific parameters and requirements.

