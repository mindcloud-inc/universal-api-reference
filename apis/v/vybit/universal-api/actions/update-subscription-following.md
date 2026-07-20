# Vybit: Update Subscription Following



```
PUT https://connect.mindcloud.co/v1/universal/vybit/latest/actions/update-subscription-following
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/update-subscription-following" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vybit/latest/actions/update-subscription-following', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | The unique key of the subscription following record. |
| `status` | string | no | Enable or disable notifications for this subscription |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessStatus` | string | no | Accept or decline a subscription invitation |
| `imageUrl` | string | no | Custom image URL for notifications |
| `linkUrl` | string | no | Custom link URL for notifications |
| `message` | string | no | Custom notification message |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "accessStatus": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "followingKey": "string",
      "imageUrl": "https://example.com",
      "linkUrl": "https://example.com",
      "message": "string",
      "ownerName": "Ava Chen",
      "sendPermissions": "string",
      "soundKey": "string",
      "soundType": "string",
      "status": "string",
      "subscriptionKey": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vybName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `accessStatus` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `followingKey` | string |  |
| `imageUrl` | string |  |
| `linkUrl` | string |  |
| `message` | string |  |
| `ownerName` | string |  |
| `sendPermissions` | string |  |
| `soundKey` | string |  |
| `soundType` | string |  |
| `status` | string |  |
| `subscriptionKey` | string |  |
| `updatedAt` | date |  |
| `vybName` | string |  |

## Native endpoint

Through the native Vybit API, this operation is `PATCH /subscription/following/{{key}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription-following.md) for the provider-specific parameters and requirements.

