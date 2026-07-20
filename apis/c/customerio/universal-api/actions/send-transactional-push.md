# Customer.io: Send Transactional Push

Sends a transactional push message from Customer.io.

```
POST https://connect.mindcloud.co/v1/universal/customerio/latest/actions/send-transactional-push
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/send-transactional-push" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionalMessageId": "password-reset",
  "identifiers": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerio/latest/actions/send-transactional-push', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionalMessageId": "password-reset",
    "identifiers": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionalMessageId` | string | yes | The transactional message template to use. You can supply the numeric template ID or the trigger name. Example: `password-reset`. |
| `identifiers` | object | yes | Identifies the person represented by your transactional message by exactly one of id, email, or cio_id. |
| `identifiers.id` | string | no | Use the customer's ID identifier when your workspace identifies people by ID. Example: `user_123`. |
| `identifiers.email` | string | no | Use the customer's email identifier when your workspace identifies people by email. Example: `user@example.com`. |
| `identifiers.cioId` | string | no | Use the immutable Customer.io person identifier. Example: `3000001`. |
| `to` | string | no | The device target for the push notification. Use all, last_used, or a specific device token. Example: `all`. |
| `title` | string | no | Overrides the transactional template title. Example: `Account alert`. |
| `message` | string | no | Overrides the transactional template message body. Example: `Your report is ready.`. |
| `imageUrl` | string | no | An image URL to show in the push notification. Example: `https://example.com/alert.png`. |
| `link` | string | no | A deep link to open when the push is tapped. Example: `myapp://reports/latest`. |
| `sound` | list<string> | no | For iOS only, controls the notification sound. One of: `default`, `none`. Example: `default`. |
| `language` | string | no | Overrides language preferences for the recipient. Example: `en`. |
| `messageData` | object | no | Key-value pairs referenced by liquid in your message. |
| `sendToUnsubscribed` | boolean | no | If false, the message is not sent to unsubscribed recipients. |
| `disableMessageRetention` | boolean | no | If true, the message body is not retained in delivery history. |
| `queueDraft` | boolean | no | If true, the message is queued as a draft instead of sent immediately. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customData` | object | no | Optional key-value pairs to attach to the push payload. |
| `customDevice` | object | no | Device information to upsert at send time. |
| `customDevice.token` | string | no | The device token for the custom device. Example: `device-token`. |
| `customDevice.platform` | list<string> | no | The device messaging platform. One of: `android`, `ios`. Example: `ios`. |
| `customDevice.lastUsed` | number | no | When the device was last used, as a unix timestamp. Example: `1772823600`. |
| `customPayload` | object | no | Raw custom push payload overrides. |
| `sendAt` | number | no | Unix timestamp determining when the message will be sent. Example: `1772823600`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryId": "string",
      "queuedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryId` | string | A unique identifier for the queued delivery. |
| `queuedAt` | number | Unix timestamp when Customer.io queued the message. |

## Native endpoint

Through the native Customer.io API, this operation is `POST /v1/send/push` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-push.md) for the provider-specific parameters and requirements.

