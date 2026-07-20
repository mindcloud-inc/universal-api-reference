# Get Outbound Message Details with Postmark

Retrieves outbound message details from Postmark.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/outbound/:messageId/details`
- **Base URL:** `https://api.postmarkapp.com`
- **Official documentation:** [Get Outbound Message Details](https://postmarkapp.com/developer/api/messages-api#outbound-message-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The Postmark outbound message ID. |
