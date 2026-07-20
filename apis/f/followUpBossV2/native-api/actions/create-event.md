# Create Event with Follow Up Boss

Creates a new event in Follow Up Boss.

## Endpoint

- **Method:** `POST`
- **Path:** `events`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [Create Event](https://docs.followupboss.com/reference/events-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | no | Lead source or website domain for the incoming event. |
| `type` | body | `string` | no | Event type, such as Registration, Property Inquiry, Seller Inquiry, or General Inquiry. |
| `message` | body | `string` | no | Message or inquiry text associated with the event. |
| `sourceUrl` | body | `string` | no | Link to the lead or event source in your system. |
| `assignedTo` | body | `string` | no | Agent name to associate with the incoming lead when applicable. |
| `person.id` | body | `string` | no | Existing Follow Up Boss person ID to attach the event to. |
| `person.firstName` | body | `string` | no | First name for the person in the event payload. |
| `person.lastName` | body | `string` | no | Last name for the person in the event payload. |
| `person.emails[].value` | body | `string` | no | Email address for the person in the event payload. |
| `person.phones[].value` | body | `string` | no | Phone number for the person in the event payload. |
