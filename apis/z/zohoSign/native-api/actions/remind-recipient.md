# Remind Recipient with Zoho Sign

Sends a reminder to a recipient in Zoho Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/requests/:requestId/remind`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Remind Recipient](https://www.zoho.com/sign/api/document-managment/remind-recipient.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Zoho Sign request identifier. |
