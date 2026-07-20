# Pushpad: Update Subscription

Updates a subscription in a Pushpad project.

```
PUT https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/update-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/update-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "subscriptionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/update-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "subscriptionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes |  |
| `subscriptionId` | number | yes |  |
| `tags[]` | array<string> | no | Accepts multiple values as an array. |
| `uid` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auth": "string",
      "createdAt": "string",
      "endpoint": "string",
      "id": 1,
      "lastClickAt": "string",
      "p256dh": "string",
      "projectId": 1,
      "tags": [
        "string"
      ],
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auth` | string |  |
| `createdAt` | string |  |
| `endpoint` | string |  |
| `id` | number |  |
| `lastClickAt` | string |  |
| `p256dh` | string |  |
| `projectId` | number |  |
| `tags` | array<string> |  |
| `uid` | string |  |

## Native endpoint

Through the native Pushpad API, this operation is `PATCH /projects/:project_id/subscriptions/:subscription_id` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription.md) for the provider-specific parameters and requirements.

