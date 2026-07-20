# Create Appointment with eTermin

Creates a new appointment in eTermin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/appointment`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Create Appointment](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Appointment/post_api_appointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `string` | yes | Start date and time of the appointment. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `end` | query | `string` | yes | End date and time of the appointment. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 19:00 |
| `calendarid` | query | `number` | yes | ID of the calendar. Use the 'Calendar - Get calendar details' function to get a list with all available calendars |
| `calendarname` | query | `string` | no | Name of the calendar (needed for Webpush) |
| `services` | query | `string` | no | ID of the service. Use the 'Service - Get service details' function to get a list with all available services. To use multiple services use a comma (,) to seperate the IDs |
| `servicestext` | query | `string` | no | Name of the services |
| `servicesinclsgtext` | query | `string` | no | Name of the services including the service groups |
| `servicesabb` | query | `string` | no | Abbreviation of the services |
| `capacity` | query | `number` | no | Defines the capacity of the appointment |
| `capused` | query | `boolean` | no | true if the capacity of the appointment needs to be checked |
| `capmaxused` | query | `number` | no | Maximum capacity that can't be exceeded |
| `location` | query | `string` | no | Location of the appointment |
| `bookingtype` | query | `string` | no | Information about how the appointment is booked |
| `bookingurl` | query | `string` | no | Information from which URL the appointment got booked |
| `checkexist` | query | `boolean` | no | Checks if the appointment start/end time is available (1 = yes, 0 = no). May not work with multiple capacity |
| `manualconfirmed` | query | `number` | no | Set to 0 to have the appointment manually confirmed by the appoinment provider |
| `confirmappointment` | query | `number` | no | Set to 1 to have the appointment manually confirmed by the booker, won't work if manualconfirmed is set to 0 |
| `confirmtime` | query | `number` | no | Time in minutes that the booker is able to confirm the appointment before it gets deleted |
| `language` | query | `string` | no | Languagecode, defines in which language the emails are sent |
| `sendemail` | query | `boolean` | no | Send a confirmation email to the adress that was specified in the email parameter (1 = yes, 0 = no) |
| `sms` | query | `boolean` | no | Send a confirmation sms to the phone number that was specified in the phone field (1 = yes, 0 = no). |
| `notificationmsg` | query | `boolean` | no | Send an information email to the appointment provider (1 = yes, 0 = no). |
| `sync` | query | `boolean` | no | True if the appointment should be synchronized with external calendars (1 = yes, 0 = no). |
| `calselid` | query | `number` | no | Use this parameter with the value -1 to also use the Calendar Linking function (also requires a valid value for the parameter services) |
| `appointmentreminderhours` | query | `number` | no | Defines when the first reminder is sent in hours (needs to be a negative value) |
| `appointmentreminderhours2` | query | `number` | no | Defines when the second reminder is sent in hours (needs to be a negative value) |
| `canceldeadline` | query | `number` | no | Minutes how long before the startdate the appointment can be cancelled |
| `recurrencerule` | query | `string` | no | Recurrence rule. e.g. DTSTART:{20171126T083000Z} DTEND:{20171126T090000Z} RRULE:FREQ=WEEKLY;INTERVAL=1;BYDAY=WE; |
| `recurrenceparentid` | query | `string` | no | ID of the parent recurring appointment |
| `pricegross` | query | `number` | no | Price including vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `pricenet` | query | `number` | no | Price excluding vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `vat` | query | `number` | no | Vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `salutation` | query | `string` | no | Salutation of the person |
| `title` | query | `string` | no | Title of the person |
| `lastname` | query | `string` | no | Lastname of the person |
| `firstname` | query | `string` | no | Firstname of the person |
| `email` | query | `string` | no | E-Mail of the person |
| `phone` | query | `string` | no | Phone of the person |
| `company` | query | `string` | no | Company of the person (make sure this field exists in your account) |
| `notes` | query | `string` | no | Appointment notes |
| `street` | query | `string` | no | Street of the person that booked appointment |
| `zip` | query | `string` | no | Zip of the person that booked appointment |
| `city` | query | `string` | no | City of the person that booked appointment |
| `customernumber` | query | `string` | no | ID of the person that booked appointment |
| `birthday` | query | `string` | no | Date of birth of the person that booked appointment |
| `additional1` | query | `string` | no | Additional appointment field 1 |
| `additional2` | query | `string` | no | Additional appointment field 2 |
| `additional3` | query | `string` | no | Additional appointment field 3 |
| `additional4` | query | `string` | no | Additional appointment field 4 |
| `additional5` | query | `string` | no | Additional appointment field 5 |
| `additional6` | query | `string` | no | Additional appointment field 6 |
| `additional7` | query | `string` | no | Additional appointment field 7 |
| `additional8` | query | `string` | no | Additional appointment field 8 |
| `additional9` | query | `string` | no | Additional appointment field 9 |
| `additional10` | query | `string` | no | Additional appointment field 10 |
| `additional11` | query | `string` | no | Additional appointment field 11 |
| `additional12` | query | `string` | no | Additional appointment field 12 |
| `additional13` | query | `string` | no | Additional appointment field 13 |
| `additional14` | query | `string` | no | Additional appointment field 14 |
| `additional15` | query | `string` | no | Additional appointment field 15 |
| `additional16` | query | `string` | no | Additional appointment field 16 |
| `additional17` | query | `string` | no | Additional appointment field 17 |
| `additional18` | query | `string` | no | Additional appointment field 18 |
| `additional19` | query | `string` | no | Additional appointment field 19 |
| `additional20` | query | `string` | no | Additional appointment field 20 |
| `agbaccepted` | query | `boolean` | no | true if customer accepted the terms of service |
| `dataprivacyaccepted` | query | `boolean` | no | true if customer accepted the privacy terms |
| `feedbackpermissionaccepted` | query | `boolean` | no | true if the customer should get a feedback mail |
| `newsletter` | query | `boolean` | no | true if the customer accepted to get newsletters |
| `bookerinfo` | query | `string` | no | Parameter that includes information for the notification message to the appointment provider |
| `emailm` | query | `number` | no | Checks if there is an email, if set to 1 |
| `lnm` | query | `number` | no | Checks if there is a lastname, if set to 1 |
| `blacklist` | query | `number` | no | Checks if the email is on the blacklist, if set to 1 |
