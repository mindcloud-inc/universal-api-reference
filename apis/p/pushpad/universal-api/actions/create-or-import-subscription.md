# Pushpad: Create or Import Subscription

Creates or imports a subscription into a Pushpad project.

```
POST https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/create-or-import-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/create-or-import-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpoint": "string",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/create-or-import-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpoint": "string",
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `auth` | string | no |  |
| `endpoint` | string | yes |  |
| `p256dh` | string | no |  |
| `projectId` | number | yes |  |
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

Through the native Pushpad API, this operation is `POST /projects/:project_id/subscriptions` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-import-subscription.md) for the provider-specific parameters and requirements.

