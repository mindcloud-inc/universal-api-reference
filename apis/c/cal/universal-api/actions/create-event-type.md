# Cal.com: Create Event Type

Creates an event type in Cal.com.

```
POST https://connect.mindcloud.co/v1/universal/cal/latest/actions/create-event-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cal.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cal/latest/actions/create-event-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lengthInMinutes": 1,
  "title": "string",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cal/latest/actions/create-event-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lengthInMinutes": 1,
    "title": "string",
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `afterEventBuffer` | number | no | Buffer after each booking, in minutes. |
| `allowReschedulingCancelledBookings` | boolean | no | Allow rescheduling for cancelled bookings. |
| `allowReschedulingPastBookings` | boolean | no | Allow rescheduling for bookings that already occurred. |
| `beforeEventBuffer` | number | no | Buffer before each booking, in minutes. |
| `bookerActiveBookingsLimit` | object | no | Concurrent active booking limit settings. |
| `bookerActiveBookingsLimit.disabled` | boolean | no | Disable active booking limits. |
| `bookerActiveBookingsLimit.maximumActiveBookings` | number | no | Maximum number of active bookings per booker. |
| `bookerActiveBookingsLimit.offerReschedule` | boolean | no | Offer reschedule option when limit is reached. |
| `bookerLayouts` | object | no | Booker layout configuration object. |
| `bookerLayouts.defaultLayout` | string | no | Default booking page layout key. |
| `bookerLayouts.enabledLayouts[]` | array<string> | no | Enabled booking page layouts. |
| `bookingFields[]` | array<object> | no | Booking field configuration objects. |
| `bookingFields[].disableOnPrefill` | boolean | no | Disable field edits when prefilled. |
| `bookingFields[].hidden` | boolean | no | Hide this booking field in forms. |
| `bookingFields[].label` | string | no | Display label for a booking field. |
| `bookingFields[].options[]` | array<string> | no | Select options for option-based booking fields. |
| `bookingFields[].placeholder` | string | no | Placeholder text for a booking field. |
| `bookingFields[].slug` | string | no | Slug identifier for a booking field. |
| `bookingFields[].type` | string | no | Booking field type discriminator. |
| `bookingLimitsCount` | object | no | Booking count limit settings. |
| `bookingLimitsCount.day` | number | no | Max bookings per day. |
| `bookingLimitsCount.disabled` | boolean | no | Disable booking count limits. |
| `bookingLimitsCount.month` | number | no | Max bookings per month. |
| `bookingLimitsCount.week` | number | no | Max bookings per week. |
| `bookingLimitsCount.year` | number | no | Max bookings per year. |
| `bookingLimitsDuration` | object | no | Rolling duration booking limits settings. |
| `bookingLimitsDuration.day` | number | no | Max booked duration per day. |
| `bookingLimitsDuration.disabled` | boolean | no | Disable duration booking limits. |
| `bookingLimitsDuration.month` | number | no | Max booked duration per month. |
| `bookingLimitsDuration.week` | number | no | Max booked duration per week. |
| `bookingLimitsDuration.year` | number | no | Max booked duration per year. |
| `bookingRequiresAuthentication` | boolean | no | Require authenticated users to book this event type. |
| `bookingWindow` | object | no | Booking window settings. |
| `bookingWindow.disabled` | boolean | no | Disable booking window restrictions. |
| `bookingWindow.rolling` | boolean | no | Use rolling booking window semantics. |
| `bookingWindow.type` | string | no | Booking window mode type. |
| `bookingWindow.value` | number | no | Booking window value for numeric mode. |
| `bookingWindow.value[]` | array<string> | no | Booking window values for list mode. |
| `calVideoSettings` | object | no | Cal Video behavior settings. |
| `calVideoSettings.disableRecordingForGuests` | boolean | no | Disable recording for guests. |
| `calVideoSettings.disableRecordingForOrganizer` | boolean | no | Disable recording for organizer. |
| `calVideoSettings.disableTranscriptionForGuests` | boolean | no | Disable transcription for guests. |
| `calVideoSettings.disableTranscriptionForOrganizer` | boolean | no | Disable transcription for organizer. |
| `calVideoSettings.enableAutomaticRecordingForOrganizer` | boolean | no | Enable automatic recording for organizer. |
| `calVideoSettings.enableAutomaticTranscription` | boolean | no | Enable automatic transcription. |
| `calVideoSettings.sendTranscriptionEmails` | boolean | no | Send transcription emails. |
| `color` | object | no | Light and dark theme color settings. |
| `color.darkThemeHex` | string | no | Hex color for dark theme. |
| `color.lightThemeHex` | string | no | Hex color for light theme. |
| `confirmationPolicy` | object | no | Confirmation policy settings. |
| `confirmationPolicy.blockUnconfirmedBookingsInBooker` | boolean | no | Block unconfirmed bookings in the booker UI. |
| `confirmationPolicy.disabled` | boolean | no | Disable confirmation policy. |
| `confirmationPolicy.noticeThreshold` | object | no | Confirmation notice threshold settings. |
| `confirmationPolicy.noticeThreshold.count` | number | no | Notice threshold amount. |
| `confirmationPolicy.noticeThreshold.unit` | string | no | Notice threshold unit. |
| `confirmationPolicy.type` | string | no | Confirmation policy mode type. |
| `customName` | string | no | Custom label for this event type. |
| `description` | string | no | Event type description. |
| `destinationCalendar` | object | no | Destination calendar integration mapping. |
| `destinationCalendar.externalId` | string | no | Destination external calendar identifier. |
| `destinationCalendar.integration` | string | no | Destination integration slug. |
| `disableCancelling` | object | no | Disable cancelling settings. |
| `disableCancelling.disabled` | boolean | no | Disable cancelling for this event type. |
| `disableGuests` | boolean | no | Disable guest invitations for this event type. |
| `disableRescheduling` | object | no | Disable rescheduling settings. |
| `disableRescheduling.disabled` | boolean | no | Disable rescheduling for this event type. |
| `disableRescheduling.minutesBefore` | number | no | Minutes before start when rescheduling becomes disabled. |
| `hidden` | boolean | no | Hide event type from public listing. |
| `hideCalendarEventDetails` | boolean | no | Hide event details in calendar entries. |
| `hideCalendarNotes` | boolean | no | Hide calendar notes on event details. |
| `hideOrganizerEmail` | boolean | no | Hide organizer email from attendees. |
| `interfaceLanguage` | string | no | Booking page interface language. |
| `lengthInMinutes` | number | yes | Duration for the event type in minutes. |
| `lengthInMinutesOptions[]` | array<number> | no | Allowed duration options in minutes. |
| `locations[]` | array<object> | no | Allowed meeting location configuration objects. |
| `locations[].address` | string | no | Address value for physical locations. |
| `locations[].integration` | string | no | Integration value for integration-backed locations. |
| `locations[].link` | string | no | Link value for URL-based locations. |
| `locations[].phone` | string | no | Phone value for phone-based locations. |
| `locations[].public` | boolean | no | Expose this location publicly. |
| `locations[].type` | string | no | Location type discriminator. |
| `lockTimeZoneToggleOnBookingPage` | boolean | no | Prevent users from changing timezone on the booking page. |
| `minimumBookingNotice` | number | no | Minimum notice before a booking can be made, in minutes. |
| `offsetStart` | number | no | Start offset in minutes. |
| `onlyShowFirstAvailableSlot` | boolean | no | Only expose the first available slot. |
| `recurrence` | object | no | Recurrence settings. |
| `recurrence.disabled` | boolean | no | Disable recurrence. |
| `recurrence.frequency` | string | no | Recurrence frequency. |
| `recurrence.interval` | number | no | Recurrence interval value. |
| `recurrence.occurrences` | number | no | Max recurrence occurrences. |
| `requiresBookerEmailVerification` | boolean | no | Require email verification before booking is completed. |
| `scheduleId` | list | no | Schedule ID assigned to the event type. |
| `seats` | object | no | Seats settings. |
| `seats.disabled` | boolean | no | Disable seats mode. |
| `seats.seatsPerTimeSlot` | number | no | Seats available per time slot. |
| `seats.showAttendeeInfo` | boolean | no | Show attendee info in seats mode. |
| `seats.showAvailabilityCount` | boolean | no | Show remaining availability count in seats mode. |
| `showOptimizedSlots` | boolean | no | Enable optimized slot suggestions. |
| `slotInterval` | number | no | Slot interval in minutes. |
| `successRedirectUrl` | string | no | Redirect URL after successful booking. |
| `useDestinationCalendarEmail` | boolean | no | Use destination calendar email when creating events. |
| `title` | string | yes | Event type title. |
| `slug` | string | yes | Event type slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookingUrl": "https://example.com",
      "currency": "string",
      "description": "string",
      "hidden": true,
      "id": 1,
      "lengthInMinutes": 1,
      "locations": [
        {}
      ],
      "metadata": {},
      "scheduleId": 1,
      "slug": "string",
      "title": "string",
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookingUrl` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `lengthInMinutes` | number |  |
| `locations` | array<object> |  |
| `metadata` | object |  |
| `scheduleId` | number |  |
| `slug` | string |  |
| `title` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Cal.com API, this operation is `POST /event-types` (base URL `https://api.cal.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-type.md) for the provider-specific parameters and requirements.

