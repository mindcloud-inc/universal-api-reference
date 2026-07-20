# Browser Use: Create Profile

Creates a profile in Browser Use.

```
POST https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/create-profile', {
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
| `name` | string | no | Optional profile name. |
| `userId` | string | no | Internal user identifier associated with the profile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Browser Use API, this operation is `POST /profiles` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-profile.md) for the provider-specific parameters and requirements.

