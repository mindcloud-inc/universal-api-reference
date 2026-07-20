# Pinghome: Create Team Notification Channel

Creates a new team notification channel in Pinghome.

```
POST https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-team-notification-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-team-notification-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "b74ca3ec-c0da-49b3-84ff-1d113b165d70",
  "type": "phone",
  "value": "+14155550124"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-team-notification-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "b74ca3ec-c0da-49b3-84ff-1d113b165d70",
    "type": "phone",
    "value": "+14155550124"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The team id that will own the notification channel. Example: `b74ca3ec-c0da-49b3-84ff-1d113b165d70`. |
| `type` | string | yes | The notification channel type, such as sms or email. Example: `phone`. |
| `value` | string | yes | The notification destination, such as an email address or phone number. Example: `+14155550124`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `POST /customer-cmd/v1/team/:id/notification-channel` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-team-notification-channel.md) for the provider-specific parameters and requirements.

