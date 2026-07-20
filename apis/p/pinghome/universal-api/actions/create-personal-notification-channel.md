# Pinghome: Create Personal Notification Channel

Creates a new personal notification channel in Pinghome.

```
POST https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-personal-notification-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-personal-notification-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "4f839792-5fc1-4d69-8fc5-842ff8304c8a",
  "type": "email",
  "value": "apps+alerts@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-personal-notification-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "4f839792-5fc1-4d69-8fc5-842ff8304c8a",
    "type": "email",
    "value": "apps+alerts@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The customer id that will own the notification channel. Example: `4f839792-5fc1-4d69-8fc5-842ff8304c8a`. |
| `type` | string | yes | The notification channel type, such as sms or email. Example: `email`. |
| `value` | string | yes | The notification destination, such as an email address or phone number. Example: `apps+alerts@mindcloud.co`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `POST /customer-cmd/v1/customer/:id/notification-channel` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-personal-notification-channel.md) for the provider-specific parameters and requirements.

