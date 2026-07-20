# Cryptlex: Update License

Updates an existing license in Cryptlex.

```
PUT https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/update-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptlex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/update-license" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptlex/latest/actions/update-license', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Unique identifier for the license. |
| `key` | string | no | Key associated with the license. |
| `notes` | string | no | Notes to store with the license. |
| `suspended` | boolean | no | Whether to suspend the license. |
| `revoked` | boolean | no | Whether to revoke the license. |
| `userId` | string | no | User linked to the license. |
| `allowedActivations` | number | no | Allowed number of activations for the license. |

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

Through the native Cryptlex API, this operation is `PATCH /v3/licenses/:id` (base URL `https://api.cryptlex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-license.md) for the provider-specific parameters and requirements.

