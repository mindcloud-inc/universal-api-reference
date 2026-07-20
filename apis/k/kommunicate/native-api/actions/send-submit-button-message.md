# Send Submit Button Message with Kommunicate

Creates a submit button message in Kommunicate.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/ws/message/v2/send`
- **Base URL:** `https://services.kommunicate.io`
- **Official documentation:** [Send Submit Button Message](https://docs.kommunicate.io/docs/message-types#submit-button)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | Conversation identifier to send the message into. |
| `message` | body | `string` | yes | Message text shown above the submit buttons. |
| `fromUserName` | body | `string` | yes | Sender user ID. |
| `payloadJson` | body | `string<object>` | yes | Array of submit button objects from the official template format. |
| `formData` | body | `object` | no | Key-value pairs submitted by the button action. |
| `formAction` | body | `string` | no | Destination URL for the submit action. |
| `requestType` | body | `string` | no | Submit encoding mode such as json. |
