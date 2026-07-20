# Cryptlex: Create License

Creates a license in Cryptlex.

```
POST https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-license" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/create-license', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Product to attach to the license. |
| `userId` | string | no | User linked to the license. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedActivations": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "key": "string",
      "productId": "string",
      "revoked": true,
      "suspended": true,
      "totalActivations": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userLocked": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedActivations` | number |  |
| `createdAt` | date |  |
| `expiresAt` | date |  |
| `id` | string |  |
| `key` | string |  |
| `productId` | string |  |
| `revoked` | boolean |  |
| `suspended` | boolean |  |
| `totalActivations` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `userLocked` | boolean |  |

## Native endpoint

Through the native Cryptlex API, this operation is `POST /v3/licenses` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-license.md) for the provider-specific parameters and requirements.

