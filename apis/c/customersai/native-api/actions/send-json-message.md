# Send JSON Message with Customers.ai

Sends a JSON message to a contact in Customers.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:recipient_id/send_json_message`
- **Base URL:** `https://api.mobilemonkey.com/public`
- **Official documentation:** [Send JSON Message](https://customers.ai/help/l/en/article/8f3i58rfxc-send-json-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient_id` | path | `string` | yes | Recipient ID or contact ID of the contact to message. |
| `json_message` | body | `object` | yes | JSON message payload to send to the contact. |
