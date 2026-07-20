# Get Sender Signature with Postmark

Retrieves a sender signature from Postmark.

## Endpoint

- **Method:** `GET`
- **Path:** `/senders/:signatureId`
- **Base URL:** `https://api.postmarkapp.com`
- **Official documentation:** [Get Sender Signature](https://postmarkapp.com/developer/api/signatures-api#sender-signature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signatureId` | path | `string` | yes | The Postmark sender signature ID. |
