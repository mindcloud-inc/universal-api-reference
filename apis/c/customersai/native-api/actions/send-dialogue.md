# Send Dialogue with Customers.ai

Sends a dialogue to a contact in Customers.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:recipient_id/send_dialogue`
- **Base URL:** `https://api.mobilemonkey.com/public`
- **Official documentation:** [Send Dialogue](https://customers.ai/help/l/en/category/doq3ewxla3-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient_id` | path | `string` | yes | Recipient ID or contact ID of the contact to message. |
| `dialogue_id` | body | `number` | yes | Dialogue ID to send to the contact. |
