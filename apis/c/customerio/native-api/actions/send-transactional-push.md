# Send Transactional Push with Customer.io

Sends a transactional push message from Customer.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send/push`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Send Transactional Push](https://docs.customer.io/integrations/api/app/#tag/Send%20Messages/operation/sendPush)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactional_message_id` | body | `string` | yes | The transactional message template to use. You can supply the numeric template ID or the trigger name. |
| `identifiers` | body | `object` | yes | Identifies the person represented by your transactional message by exactly one of id, email, or cio_id. |
| `identifiers.id` | body | `string` | no | Use the customer's ID identifier when your workspace identifies people by ID. |
| `identifiers.email` | body | `string` | no | Use the customer's email identifier when your workspace identifies people by email. |
| `identifiers.cio_id` | body | `string` | no | Use the immutable Customer.io person identifier. |
| `to` | body | `string` | no | The device target for the push notification. Use all, last_used, or a specific device token. |
| `title` | body | `string` | no | Overrides the transactional template title. |
| `message` | body | `string` | no | Overrides the transactional template message body. |
| `image_url` | body | `string` | no | An image URL to show in the push notification. |
| `link` | body | `string` | no | A deep link to open when the push is tapped. |
| `sound` | body | `list<string>` | no | For iOS only, controls the notification sound. Accepted values: `default`, `none`. |
| `custom_data` | body | `object` | no | Optional key-value pairs to attach to the push payload. |
| `custom_device` | body | `object` | no | Device information to upsert at send time. |
| `customDevice.token` | body | `string` | no | The device token for the custom device. |
| `customDevice.platform` | body | `list<string>` | no | The device messaging platform. Accepted values: `android`, `ios`. |
| `custom_device.last_used` | body | `number` | no | When the device was last used, as a unix timestamp. |
| `custom_payload` | body | `object` | no | Raw custom push payload overrides. |
| `language` | body | `string` | no | Overrides language preferences for the recipient. |
| `message_data` | body | `object` | no | Key-value pairs referenced by liquid in your message. |
| `send_at` | body | `number` | no | Unix timestamp determining when the message will be sent. |
| `send_to_unsubscribed` | body | `boolean` | no | If false, the message is not sent to unsubscribed recipients. |
| `disable_message_retention` | body | `boolean` | no | If true, the message body is not retained in delivery history. |
| `queue_draft` | body | `boolean` | no | If true, the message is queued as a draft instead of sent immediately. |
