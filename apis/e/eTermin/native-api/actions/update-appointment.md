# Update Appointment with eTermin

Updates an existing appointment in eTermin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/appointment`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Update Appointment](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Appointment/put_api_appointment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | ID of the appointment that you want to modify. |
| `start` | query | `date` | no | Start date and time of the appointment. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `end` | query | `date` | no | End date and time of the appointment. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 19:00 |
| `calendarid` | query | `number` | no | ID of the calendar. |
| `calendarname` | query | `string` | no | Name of the calendar (needed for Webpush) |
| `services` | query | `string` | no | ID of the service. Use the 'Service - Get service details' function to get a list with all available services. To use multiple services use a comma (,) to seperate the IDs |
| `servicestext` | query | `string` | no | Name of the services |
| `servicesinclsgtext` | query | `string` | no | Name of the services including the service groups |
| `servicesabb` | query | `string` | no | Abbreviation of the services |
| `capacity` | query | `number` | no | Defines the capacity of the appointment |
| `location` | query | `string` | no | Location of the appointment |
| `manualconfirmed` | query | `number` | no | Set to 0 to have the appointment manually confirmed by the appoinment provider, set to 1 if the appointment got confirmed |
| `sendemail` | query | `boolean` | no | Send a confirmation email to the adress that was specified in the email parameter (1 = yes, 0 = no). |
| `msgtype` | query | `boolean` | no | ID of the template that is sent to the customer with the API call |
| `notificationmsg` | query | `boolean` | no | Send an information email to the appointment provider (1 = yes, 0 = no). |
| `sync` | query | `boolean` | no | True if the appointment should be synchronized with external calendars (1 = yes, 0 = no). |
| `appointmentreminderhours` | query | `number` | no | Defines when the first reminder is sent in hours (needs to be a negative value) |
| `appointmentreminderhours2` | query | `number` | no | Defines when the second reminder is sent in hours (needs to be a negative value) |
| `canceldeadline` | query | `number` | no | Minutes how long before the startdate the appointment can be cancelled |
| `recurrencerule` | query | `string` | no | Recurrence rule. e.g. DTSTART:20171126T083000Z DTEND:20181126T090000Z RRULE:FREQ=WEEKLY;INTERVAL=1;BYDAY=WE; |
| `pricegross` | query | `number` | no | Price including vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `pricenet` | query | `number` | no | Price excluding vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `vat` | query | `number` | no | Vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `linkedappidmanual` | query | `number` | no | AppID of the linked app if the calendar linking should be applied after two appointments are booked. Keep in mind to update the second appointment aswell |
| `salutation` | query | `string` | no | Salutation of the person. |
| `title` | query | `string` | no | Title of the person. |
| `lastname` | query | `string` | no | Lastname of the person. |
| `firstname` | query | `string` | no | Firstname of the person. |
| `email` | query | `string` | no | E-Mail of the person. |
| `phone` | query | `string` | no | Phone of the person. |
| `company` | query | `string` | no | Company of the person (make sure this field exists in your account) |
| `notes` | query | `string` | no | Appointment notes. |
| `street` | query | `string` | no | Street. |
| `zip` | query | `string` | no | Zip. |
| `city` | query | `string` | no | City. |
| `customernumber` | query | `string` | no | ID of the person that booked appointment. |
| `additional1` | query | `string` | no | Additional appointment field 1. |
| `additional2` | query | `string` | no | Additional appointment field 2. |
| `additional3` | query | `string` | no | Additional appointment field 3. |
| `additional4` | query | `string` | no | Additional appointment field 4. |
| `additional5` | query | `string` | no | Additional appointment field 5. |
| `additional6` | query | `string` | no | Additional appointment field 6. |
| `additional7` | query | `string` | no | Additional appointment field 7. |
| `additional8` | query | `string` | no | Additional appointment field 8. |
| `additional9` | query | `string` | no | Additional appointment field 9. |
| `additional10` | query | `string` | no | Additional appointment field 10. |
| `additional11` | query | `string` | no | Additional appointment field 11. |
| `additional12` | query | `string` | no | Additional appointment field 12. |
| `additional13` | query | `string` | no | Additional appointment field 13. |
| `additional14` | query | `string` | no | Additional appointment field 14. |
| `additional15` | query | `string` | no | Additional appointment field 15. |
| `additional16` | query | `string` | no | Additional appointment field 16. |
| `additional17` | query | `string` | no | Additional appointment field 17. |
| `additional18` | query | `string` | no | Additional appointment field 18. |
| `additional19` | query | `string` | no | Additional appointment field 19. |
| `additional20` | query | `string` | no | Additional appointment field 20. |
