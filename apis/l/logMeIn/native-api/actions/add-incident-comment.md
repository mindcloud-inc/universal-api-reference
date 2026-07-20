# Add Incident Comment with LogMeIn

Creates a new incident comment in LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/goto-resolve-ticketing/v1/incidents/:referenceNum/comments`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Add Incident Comment](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceNum` | path | `string` | yes | Required incident reference number. |
| `comment` | body | `string` | yes | Comment text. |
| `hiddenFromCustomerAt` | body | `date` | no | Timestamp marking the comment hidden from customer. |
| `attachments[]` | body | `array<object>` | no | Optional comment attachments. |
