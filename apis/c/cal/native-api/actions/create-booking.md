# Create Booking with Cal.com

Creates a booking in Cal.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/bookings`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Create Booking](https://cal.com/docs/api-reference/v2/bookings/create-a-booking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | body | `string` | yes | Booking start time in ISO 8601 UTC format. |
| `attendee` | body | `object` | yes | Attendee object including at least name and timeZone. |
| `attendee.name` | body | `string` | yes | Attendee full name. |
| `attendee.email` | body | `string` | no | Attendee email address. |
| `attendee.timeZone` | body | `string` | yes | Attendee IANA time zone. |
| `attendee.language` | body | `string` | no | Attendee language code. |
| `attendee.phoneNumber` | body | `string` | no | Attendee phone number. |
| `eventTypeId` | body | `list` | no | Event type ID to book when using ID-based routing. |
| `eventTypeSlug` | body | `list` | no | Event type slug to book when using slug-based routing. |
| `username` | body | `string` | no | Username owner for the event type route. |
| `teamSlug` | body | `string` | no | Team slug for team-scoped booking routes. |
| `organizationSlug` | body | `string` | no | Organization slug for org-scoped booking routes. |
| `guests[]` | body | `array<string>` | no | Guest email list to include in the booking. |
| `meetingUrl` | body | `string` | no | Override meeting URL for this booking. |
| `location` | body | `object` | no | Booking location payload. |
| `location.type` | body | `string` | no | Location type discriminator. |
| `location.location` | body | `string` | no | Location value for custom location types. |
| `location.address` | body | `string` | no | Address value when using physical/in-person location types. |
| `location.phone` | body | `string` | no | Phone number when using phone location types. |
| `location.integration` | body | `string` | no | Integration identifier for integration-backed location types. |
| `bookingFieldsResponses` | body | `object` | no | Dynamic booking field responses map. |
| `metadata` | body | `object` | no | Custom metadata object for the booking. |
| `lengthInMinutes` | body | `number` | no | Override booking duration in minutes. |
| `routing` | body | `object` | no | Routing payload for round-robin or queued routing. |
| `routing.queuedResponseId` | body | `string` | no | Queued routing response identifier. |
| `routing.responseId` | body | `number` | no | Routing response identifier. |
| `routing.teamMemberIds[]` | body | `array<number>` | no | Candidate team member IDs for routing. |
| `routing.teamMemberEmail` | body | `string` | no | Team member email for routing. |
| `routing.skipContactOwner` | body | `boolean` | no | Skip assigning the contact owner during routing. |
| `routing.crmAppSlug` | body | `string` | no | CRM app slug used by routing rules. |
| `routing.crmOwnerRecordType` | body | `string` | no | CRM owner record type used in routing. |
| `emailVerificationCode` | body | `string` | no | Email verification code for protected event types. |
| `instant` | body | `boolean` | no | Create instant booking when supported. |
| `recurrenceCount` | body | `number` | no | Recurring booking count for recurring event types. |
