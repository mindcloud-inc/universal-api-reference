# Create Event Type with Cal.com

Creates an event type in Cal.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/event-types`
- **Base URL:** `https://api.cal.com/v2`
- **Official documentation:** [Create Event Type](https://cal.com/docs/api-reference/v2/event-types/create-an-event-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `afterEventBuffer` | body | `number` | no | Buffer after each booking, in minutes. |
| `allowReschedulingCancelledBookings` | body | `boolean` | no | Allow rescheduling for cancelled bookings. |
| `allowReschedulingPastBookings` | body | `boolean` | no | Allow rescheduling for bookings that already occurred. |
| `beforeEventBuffer` | body | `number` | no | Buffer before each booking, in minutes. |
| `bookerActiveBookingsLimit` | body | `object` | no | Concurrent active booking limit settings. |
| `bookerActiveBookingsLimit.disabled` | body | `boolean` | no | Disable active booking limits. |
| `bookerActiveBookingsLimit.maximumActiveBookings` | body | `number` | no | Maximum number of active bookings per booker. |
| `bookerActiveBookingsLimit.offerReschedule` | body | `boolean` | no | Offer reschedule option when limit is reached. |
| `bookerLayouts` | body | `object` | no | Booker layout configuration object. |
| `bookerLayouts.defaultLayout` | body | `string` | no | Default booking page layout key. |
| `bookerLayouts.enabledLayouts[]` | body | `array<string>` | no | Enabled booking page layouts. |
| `bookingFields[]` | body | `array<object>` | no | Booking field configuration objects. |
| `bookingFields[].disableOnPrefill` | body | `boolean` | no | Disable field edits when prefilled. |
| `bookingFields[].hidden` | body | `boolean` | no | Hide this booking field in forms. |
| `bookingFields[].label` | body | `string` | no | Display label for a booking field. |
| `bookingFields[].options[]` | body | `array<string>` | no | Select options for option-based booking fields. |
| `bookingFields[].placeholder` | body | `string` | no | Placeholder text for a booking field. |
| `bookingFields[].slug` | body | `string` | no | Slug identifier for a booking field. |
| `bookingFields[].type` | body | `string` | no | Booking field type discriminator. |
| `bookingLimitsCount` | body | `object` | no | Booking count limit settings. |
| `bookingLimitsCount.day` | body | `number` | no | Max bookings per day. |
| `bookingLimitsCount.disabled` | body | `boolean` | no | Disable booking count limits. |
| `bookingLimitsCount.month` | body | `number` | no | Max bookings per month. |
| `bookingLimitsCount.week` | body | `number` | no | Max bookings per week. |
| `bookingLimitsCount.year` | body | `number` | no | Max bookings per year. |
| `bookingLimitsDuration` | body | `object` | no | Rolling duration booking limits settings. |
| `bookingLimitsDuration.day` | body | `number` | no | Max booked duration per day. |
| `bookingLimitsDuration.disabled` | body | `boolean` | no | Disable duration booking limits. |
| `bookingLimitsDuration.month` | body | `number` | no | Max booked duration per month. |
| `bookingLimitsDuration.week` | body | `number` | no | Max booked duration per week. |
| `bookingLimitsDuration.year` | body | `number` | no | Max booked duration per year. |
| `bookingRequiresAuthentication` | body | `boolean` | no | Require authenticated users to book this event type. |
| `bookingWindow` | body | `object` | no | Booking window settings. |
| `bookingWindow.disabled` | body | `boolean` | no | Disable booking window restrictions. |
| `bookingWindow.rolling` | body | `boolean` | no | Use rolling booking window semantics. |
| `bookingWindow.type` | body | `string` | no | Booking window mode type. |
| `bookingWindow.value` | body | `number` | no | Booking window value for numeric mode. |
| `bookingWindow.value[]` | body | `array<string>` | no | Booking window values for list mode. |
| `calVideoSettings` | body | `object` | no | Cal Video behavior settings. |
| `calVideoSettings.disableRecordingForGuests` | body | `boolean` | no | Disable recording for guests. |
| `calVideoSettings.disableRecordingForOrganizer` | body | `boolean` | no | Disable recording for organizer. |
| `calVideoSettings.disableTranscriptionForGuests` | body | `boolean` | no | Disable transcription for guests. |
| `calVideoSettings.disableTranscriptionForOrganizer` | body | `boolean` | no | Disable transcription for organizer. |
| `calVideoSettings.enableAutomaticRecordingForOrganizer` | body | `boolean` | no | Enable automatic recording for organizer. |
| `calVideoSettings.enableAutomaticTranscription` | body | `boolean` | no | Enable automatic transcription. |
| `calVideoSettings.sendTranscriptionEmails` | body | `boolean` | no | Send transcription emails. |
| `color` | body | `object` | no | Light and dark theme color settings. |
| `color.darkThemeHex` | body | `string` | no | Hex color for dark theme. |
| `color.lightThemeHex` | body | `string` | no | Hex color for light theme. |
| `confirmationPolicy` | body | `object` | no | Confirmation policy settings. |
| `confirmationPolicy.blockUnconfirmedBookingsInBooker` | body | `boolean` | no | Block unconfirmed bookings in the booker UI. |
| `confirmationPolicy.disabled` | body | `boolean` | no | Disable confirmation policy. |
| `confirmationPolicy.noticeThreshold` | body | `object` | no | Confirmation notice threshold settings. |
| `confirmationPolicy.noticeThreshold.count` | body | `number` | no | Notice threshold amount. |
| `confirmationPolicy.noticeThreshold.unit` | body | `string` | no | Notice threshold unit. |
| `confirmationPolicy.type` | body | `string` | no | Confirmation policy mode type. |
| `customName` | body | `string` | no | Custom label for this event type. |
| `description` | body | `string` | no | Event type description. |
| `destinationCalendar` | body | `object` | no | Destination calendar integration mapping. |
| `destinationCalendar.externalId` | body | `string` | no | Destination external calendar identifier. |
| `destinationCalendar.integration` | body | `string` | no | Destination integration slug. |
| `disableCancelling` | body | `object` | no | Disable cancelling settings. |
| `disableCancelling.disabled` | body | `boolean` | no | Disable cancelling for this event type. |
| `disableGuests` | body | `boolean` | no | Disable guest invitations for this event type. |
| `disableRescheduling` | body | `object` | no | Disable rescheduling settings. |
| `disableRescheduling.disabled` | body | `boolean` | no | Disable rescheduling for this event type. |
| `disableRescheduling.minutesBefore` | body | `number` | no | Minutes before start when rescheduling becomes disabled. |
| `hidden` | body | `boolean` | no | Hide event type from public listing. |
| `hideCalendarEventDetails` | body | `boolean` | no | Hide event details in calendar entries. |
| `hideCalendarNotes` | body | `boolean` | no | Hide calendar notes on event details. |
| `hideOrganizerEmail` | body | `boolean` | no | Hide organizer email from attendees. |
| `interfaceLanguage` | body | `string` | no | Booking page interface language. |
| `lengthInMinutes` | body | `number` | yes | Duration for the event type in minutes. |
| `lengthInMinutesOptions[]` | body | `array<number>` | no | Allowed duration options in minutes. |
| `locations[]` | body | `array<object>` | no | Allowed meeting location configuration objects. |
| `locations[].address` | body | `string` | no | Address value for physical locations. |
| `locations[].integration` | body | `string` | no | Integration value for integration-backed locations. |
| `locations[].link` | body | `string` | no | Link value for URL-based locations. |
| `locations[].phone` | body | `string` | no | Phone value for phone-based locations. |
| `locations[].public` | body | `boolean` | no | Expose this location publicly. |
| `locations[].type` | body | `string` | no | Location type discriminator. |
| `lockTimeZoneToggleOnBookingPage` | body | `boolean` | no | Prevent users from changing timezone on the booking page. |
| `minimumBookingNotice` | body | `number` | no | Minimum notice before a booking can be made, in minutes. |
| `offsetStart` | body | `number` | no | Start offset in minutes. |
| `onlyShowFirstAvailableSlot` | body | `boolean` | no | Only expose the first available slot. |
| `recurrence` | body | `object` | no | Recurrence settings. |
| `recurrence.disabled` | body | `boolean` | no | Disable recurrence. |
| `recurrence.frequency` | body | `string` | no | Recurrence frequency. |
| `recurrence.interval` | body | `number` | no | Recurrence interval value. |
| `recurrence.occurrences` | body | `number` | no | Max recurrence occurrences. |
| `requiresBookerEmailVerification` | body | `boolean` | no | Require email verification before booking is completed. |
| `scheduleId` | body | `list` | no | Schedule ID assigned to the event type. |
| `seats` | body | `object` | no | Seats settings. |
| `seats.disabled` | body | `boolean` | no | Disable seats mode. |
| `seats.seatsPerTimeSlot` | body | `number` | no | Seats available per time slot. |
| `seats.showAttendeeInfo` | body | `boolean` | no | Show attendee info in seats mode. |
| `seats.showAvailabilityCount` | body | `boolean` | no | Show remaining availability count in seats mode. |
| `showOptimizedSlots` | body | `boolean` | no | Enable optimized slot suggestions. |
| `slotInterval` | body | `number` | no | Slot interval in minutes. |
| `successRedirectUrl` | body | `string` | no | Redirect URL after successful booking. |
| `useDestinationCalendarEmail` | body | `boolean` | no | Use destination calendar email when creating events. |
| `title` | body | `string` | yes | Event type title. |
| `slug` | body | `string` | yes | Event type slug. |
