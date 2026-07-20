# Send Event with Loops

Creates an event in Loops for a contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/send`
- **Base URL:** `https://app.loops.so/api/v1`
- **Official documentation:** [Send Event](https://loops.so/docs/api-reference/send-event)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventName` | body | `string` | yes |
| `email` | body | `string` | no |
| `userId` | body | `string` | no |
| `eventProperties` | body | `object` | no |
| `mailingLists` | body | `object` | no |
