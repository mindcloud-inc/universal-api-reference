# Send Reminder with Xodo Sign

Sends a reminder to a document signer in Xodo Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/send_reminder`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Send Reminder](https://eversign.com/api/documentation/methods#send-reminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | Business ID to scope the reminder request. |
| `document_hash` | body | `string` | yes | Unique document hash to send a reminder for. |
| `signer_id` | body | `string` | yes | Signer ID that should receive the reminder. |
