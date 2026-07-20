# Update Customer with LiveChat

Updates an existing customer in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/update_customer`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Update Customer](https://platform.text.com/docs/messaging/agent-chat-api#update-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The customer UUID v4. |
| `name` | body | `string` | no | The customer's name. |
| `email` | body | `string` | no | The customer's email. |
| `avatar` | body | `string` | no | The URL of the customer's avatar. |
| `phone_number` | body | `string` | no | The customer's phone number in E.164 format. |
| `session_fields[]` | body | `array<object>` | no | Custom session field objects in array order. |
| `omnichannel` | body | `object` | no | Omnichannel customer data. |
| `omnichannel.fbmessenger` | body | `object` | no | Facebook Messenger customer data. |
| `omnichannel.fbmessenger.id` | body | `string` | no | Facebook Messenger user ID. |
| `omnichannel.twilio` | body | `object` | no | Twilio customer data. |
| `omnichannel.twilio.phone_number` | body | `string` | no | Twilio phone number. |
