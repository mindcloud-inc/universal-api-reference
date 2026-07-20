# Create Event with Trak Qr Automation

Creates a new event in Trak Qr Automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/events`
- **Base URL:** `https://backend.trak.codes/api/v0`
- **Official documentation:** [Create Event](https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Event user-facing name, used as app title in Trak. |
| `eventId` | body | `string` | yes | Your internal event ID, used as correlation ID. |
| `formFields[]` | body | `array<object>` | yes | Schema of attendee attachment fields for this event. |
| `name` | body | `string` | yes | Field name used as label and report column header. |
| `editor` | body | `list` | yes | Field type: number, line, text, select, radios, or checkboxes. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `values[]` | body | `array<string>` | no | Allowed values for select, radios, and checkboxes fields. Send multiple values as a array. |
| `titleFormat` | body | `string` | no | Mini-template for ticket titles, such as {First name} {Last name}. |
| `logoUrl` | body | `string` | no | Optional PNG or JPG logo URL for tickets, ideally 300x300px with a white background. |
| `bgUrl` | body | `string` | no | Optional PNG or JPG ticket background URL, ideally 596x842px. |
| `creatorInfo` | body | `object` | no | Optional information about the form creator. |
| `ip` | body | `string` | no | Creator IP address. |
| `loc` | body | `string` | no | Creator country or town. |
| `email` | body | `string` | no | Creator email used for support. |
