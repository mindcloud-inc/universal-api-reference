# Create Attendee with Trak Qr Automation

Creates a new attendee for an event in Trak Qr Automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:eventKey/attendees`
- **Base URL:** `https://backend.trak.codes/api/v0`
- **Official documentation:** [Create Attendee](https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventKey` | path | `string` | yes | Generated event key returned by Create Event. |
| `notes` | body | `string` | no | Optional comments on the attendee. |
| `attachments[]` | body | `array<object>` | yes | Attendee form data fields. |
| `kind` | body | `string` | yes | Attachment field name matching an event form field. |
| `val` | body | `string` | yes | Attachment field value. Trak accepts a number, string, or string array. |
| `internal` | body | `boolean` | no | Set true for technical fields that should not be shown in the Trak UI. |
