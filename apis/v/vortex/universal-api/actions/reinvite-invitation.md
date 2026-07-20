# Vortex: Reinvite Invitation



```
PUT https://connect.mindcloud.co/v1/universal/vortex/latest/actions/reinvite-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vortex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vortex/latest/actions/reinvite-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vortex/latest/actions/reinvite-invitation', {
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
      "accountId": "string",
      "createdAt": "string",
      "deactivated": true,
      "expired": true,
      "expires": "string",
      "id": "string",
      "invitationType": "string",
      "modifiedAt": "string",
      "scope": "string",
      "scopeType": "string",
      "status": "string",
      "target": [
        {
          "avatarUrl": "https://example.com",
          "name": "Ava Chen",
          "type": "string",
          "value": "string"
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
| `accountId` | string |  |
| `createdAt` | string |  |
| `deactivated` | boolean |  |
| `expired` | boolean |  |
| `expires` | string |  |
| `id` | string |  |
| `invitationType` | string |  |
| `modifiedAt` | string |  |
| `scope` | string |  |
| `scopeType` | string |  |
| `status` | string |  |
| `target[].avatarUrl` | string |  |
| `target[].name` | string |  |
| `target[].type` | string |  |
| `target[].value` | string |  |

## Native endpoint

Through the native Vortex API, this operation is `POST /api/v1/invitations/{invitationId}/reinvite` (base URL `https://api.vortexsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reinvite-invitation.md) for the provider-specific parameters and requirements.

