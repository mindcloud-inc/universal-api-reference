# Send Signer Reminder with RightSignature

Sends a reminder email to a pending RightSignature signer.

## Endpoint

- **Method:** `POST`
- **Path:** `/signers/:id/reminders`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Send Signer Reminder](https://api.rightsignature.com/documentation/resources/v2/signers/reminders.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Signer ID |
