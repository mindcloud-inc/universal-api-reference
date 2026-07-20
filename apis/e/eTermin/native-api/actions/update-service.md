# Update Service with eTermin

Updates an existing service in eTermin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/service`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Update Service](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Service/put_api_service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | ID of the service |
| `servicegroupid` | query | `number` | no | ID of the service group |
| `servicede` | query | `string` | no | Name of the service in german. For other languages use serviceLANGUAGECODE e.g. serviceen |
| `timeslotminutes` | query | `number` | no | Duration of the service in minutes |
| `infode` | query | `string` | no | Additional description of the service in german. For other languages use serviceLANGUAGECODE e.g. infoen |
| `infodisplay` | query | `number` | no | Defines where the information is shown (0 = below service name, 1 = informationtext page 2, 2 = summary after booking, 3 = below service name and summary after booking) |
| `differenttimeresource` | query | `boolean` | no | True if you want to add pre- or post processing times |
| `timeslotminutesresstart` | query | `number` | no | Busy by minute (use negative number to have a pre-processing time) |
| `timeslotminutesresend` | query | `number` | no | Busy until minute (use a number greater than timeslotminutes to have a post-processing time) |
| `price` | query | `number` | no | Price of the service |
| `priceispercentage` | query | `boolean` | no | True if price is a percentage |
| `abbreviation` | query | `string` | no | abbreviation of the service |
| `enablecapacity` | query | `boolean` | no | True to enable the capacity of the service |
| `showcapselectionbox` | query | `boolean` | no | True if the customer is able to select the capacity |
| `maxcapacity` | query | `number` | no | Sets the maximum capacity of the service |
| `maxcapacityusersel` | query | `number` | no | Sets the maximum capacity the user can set on the booking page (needs showcapselectionbox to be true) |
| `capacitynonsel` | query | `number` | no | Sets the capacity if selected on the booking page (needs showcapselectionbox to be false) |
| `image` | query | `string` | no | Image of the service |
| `appdeadline` | query | `number` | no | Time the appointment must be booked in advance in minutes |
| `appfuture` | query | `number` | no | Time the appointment can be booked in the future in days |
| `startedapp` | query | `number` | no | Time the appointment can be booked if already started in minutes (has to be a negative value) |
| `canceldeadline` | query | `number` | no | Time the appointment can be cancelled in hours |
| `dayselectiontype` | query | `number` | no | Defines how page 2 shows the available days (0 = Calendar, 1 = list of days) |
| `appointmentlocation` | query | `number` | no | Defines the location of the appointment |
| `appointmentlocationtext` | query | `string` | no | Defines the location text if appointmentlocation = 3 |
| `vendorconfirmation` | query | `number` | no | Defines if the appointment provider needs to manually confirm the appointment (0 = manually, 1 = automatically) |
| `smsconfirmation` | query | `number` | no | Defines if a SMS confirmation is sent after booking (1 = enabled, 0 = disabled) |
| `reminderhours` | query | `number` | no | Defines when the first reminder is sent in hours (needs to be a negative value) |
| `reminderhours2` | query | `number` | no | Defines when the second reminder is sent in hours (needs to be a negative value) |
| `cluster` | query | `number` | no | Defines if the cluster is applied to this service (1 = enabled, 0 = disabled) |
| `customerconfirm` | query | `number` | no | Defines if the customer needs to confirm the appointment (1 = enabled, 0 = disabled; doesn't work with online payments or vendorconfirmation) |
| `customerconfirmtime` | query | `number` | no | Time in minutes the customer has time to confirm the appointment (customerconfirm must be set to 1) |
| `PM0` | query | `number` | no | Shows online payment options (1 = enabled, 0 = disabled) |
| `PM1` | query | `number` | no | Shows on site payment options (1 = enabled, 0 = disabled) |
| `PM2` | query | `number` | no | Shows by invoice payment options (1 = enabled, 0 = disabled) |
| `paymentamountpercentage` | query | `number` | no | Defines the payment amount that needs to be paid at the end of booking |
| `paymentamountisabsolute` | query | `number` | no | Defines if paymentamountpercentage is abolute or a percentage (1 = absolute, 0 = percentage) |
| `currency` | query | `string` | no | Defines the currency of the service |
| `voucherfield` | query | `number` | no | Defines if the voucherfield is shown (0 = not shown, 1 = shown, 2 = shown and mandatory) |
| `mpbs` | query | `number` | no | Defines if the price is multiplied by the amount of booked appointments |
| `timeslotformat` | query | `number` | no | Defines how the timeslots are shown on page 2 on the bookingpage (0 = starttime - endtime, 1 = starttime, 2 = only date, 3 = calendar week, 4 = like 0 but with dates, 5 = startdate only) |
| `multiappointment` | query | `number` | no | Defines if multiple appointments can be booked in one booking (0 = no, 1 = yes) |
| `multiservicedurationcalcmethod` | query | `number` | no | Defines how the duration is calculated if multiple services are selected (0 = all durations are summed up, 1 = only duration of the longest service, 2 = all durations are halfed, 3 = like 2 except the longest service) |
| `calendarselection` | query | `number` | no | Defines if the calendar selection should be shown (0 = no, 1 = yes) |
| `ssca` | query | `number` | no | Defines if in the calendar selection the entry all calendars is shown (0 = no, 1 = yes) |
| `showcalname` | query | `number` | no | Defines if in the calendar name is shown in the time slot (0 = no, 1 = yes) |
| `showcalpic` | query | `number` | no | Defines if in the calendar picture is shown after the timeslot is selected (0 = no, 1 = yes) |
| `showavcap` | query | `number` | no | Defines if the available capacity is shown in time slots (0 = no, 1 = yes) |
| `limitbooking` | query | `number` | no | Defines if this service can be booked a limited amount of times per customer (0 = no, 1 = yes) |
| `limitappointmentstype` | query | `number` | no | Defines how the appointments are limited (0 = per booking day, 1 = per week, 2 = per month, 3 = per year, 4 = per booked day) |
| `limitappointments` | query | `number` | no | Defines how many appointments can be booked per customer |
| `limitservice` | query | `number` | no | Defines if the limitation only applies to this specific service |
| `wowing` | query | `number` | no | Set to 0 if the Wowing interface should be disabled for this service |
| `wowingautomationid` | query | `number` | no | Defines the Woing Automation ID |
| `paymentduration` | query | `number` | no | Defines the payment term for LexOffice |
| `workloadperc` | query | `number` | no | Defines the percentage of time slots that are not shown |
| `nrtimeslotentries` | query | `number` | no | Defines the maximum amount of time slots that are shown |
| `feedback` | query | `number` | no | Set to 0 if the feedback checkbox should not be shown |
| `calcdrivingtime` | query | `number` | no | Defines if driving time should be calculated (0 = no, 1 = yes) |
| `fillcalendarstrategy` | query | `number` | no | Defines how the calender should be filled (0 = standard, 1 = random, 2 = round Robin, 3 = sequential, 4 = skills, 5 = strict round Robin) |
| `waitinglist` | query | `number` | no | Defines if the waiting list should be available (0 = no, 1 = yes) |
| `notearlyapp` | query | `number` | no | Defines if the customer should get an email if an earlier appointment is available (0 = not active, 1 = for appointments that were cancelled online, 2 = for appointments cancelled online and manually, 3 = like 1 but per calendar, 4 = like 2 but per calendar) |
| `sortorder` | query | `number` | no | Defines the position in the servicegroup |
| `bookingtype` | query | `number` | no | Defines the bookingtype (0 = appointment, 1 = no appointment booking allowed, 2 = 'negative' appointment, 3 = reservation list, 4 = voucher sale) |
| `showinternal` | query | `boolean` | no | Defines if the service is shown in the backend |
| `enabled` | query | `boolean` | no | Defines if the service is shown in the frontend |
| `showindb` | query | `boolean` | no | Defines if the service is shown in the most booked area of the Dashboard |
| `emailsender` | query | `string` | no | Defines the sender adress of the email for this service |
| `emailtxtde` | query | `string` | no | A special placeholder %SERVICETEXT% for emails, use other language codes to set the text (for example emailtxten for english) |
| `infotxtp2` | query | `string` | no | A special placeholder %INFOTEXTP2% for page 2 of the booking page |
| `pricesuffixde` | query | `string` | no | Additional information for the price, use other language codes to set the text (for example emailtxten for english) |
| `priceinfopos` | query | `number` | no | Defines where the pricesuffix is shown (0 = left side, 1 = right side) |
| `vat` | query | `number` | no | Defines the vat rate of the service |
| `multiplypricewithcap` | query | `boolean` | no | Defines if the price is multiplied with the capacity |
| `pricediffperday` | query | `boolean` | no | Defines if different prices per weekday are applied |
| `issubscription` | query | `boolean` | no | Defines if the service is a subscription |
| `capseltextde` | query | `string` | no | Defines the text if there is a capacity selection on that service, use other language codes to set the text (for example capseltexten for english) |
| `mstextpos` | query | `number` | no | Defines the position of capseltext (0 = above selection, 1 = to the right) |
| `allowonlythisservice` | query | `boolean` | no | If there are multiple services with capacity available at the same time, this option prevents that they will get mixed, if set to true |
| `multiservicesel` | query | `boolean` | no | True, if the service can be booked multiple times after another. This won't work if the parameter enablecapacity is true aswell |
| `multiservicemin` | query | `number` | no | Defines the minimum amount that can be choosen for multi service selection |
| `multiservicemax` | query | `number` | no | Defines the maximum amount that can be choosen for multi service selection |
| `extramin` | query | `number` | no | Defines total wrap up time |
| `extramintype` | query | `number` | no | 0 if extramin should not be applied if differenttimeresource is true, 1 if extramin should be added to timeslotminutesresend |
| `maxappsel` | query | `number` | no | Defines the maximum amount of appointments that can be selected on the booking page if multiappointment is true (in this service or globally) |
| `nrappsel` | query | `number` | no | Defines the maximum / minimum amount of appointments that MUST be selected on the booking page if multiappointment is true (in this service or globally) |
| `maxminslots` | query | `boolean` | no | Defines if nrappsel is maximum (0) or minimum (1) |
| `nrappseladjacent` | query | `boolean` | no | True, if the selected appointments have to be adjacent |
| `nrappseladjacenttype` | query | `number` | no | 0 = the date and time need to be adjacent, 1 = only the day need to be adjacent |
| `specificrangenextslot` | query | `boolean` | no | True, if the next appointment needs to be after a specific timeframe |
| `rangestart` | query | `number` | no | Days after the last appoinment |
| `rangeend` | query | `number` | no | Days range for the new appointment |
| `infotextinslots` | query | `boolean` | no | True, if the info text should be shown in the slot text in page 2 of the booking page |
| `appattrib` | query | `number` | no | Defines which attribute is set automatically in appointment. Attributes are binary encoded (1st attribute = 1, 2nd = 2, 3rd = 4; 1st + 2nd = 3) |
| `addapphours` | query | `number` | no | Hours after the first appointment, where a second appointment is booked |
| `rrule` | query | `string` | no | Defines the RRULE for this service |
| `bookingminute` | query | `number` | no | Defines when the timeslots are shown (61 = no restrictions, 0 = every full hour, 31 = every full and half hour, 15 or 30 or 45 = x minutes after a full hour) |
| `showserviceids` | query | `string` | no | Service(s) that have to be selected to show this service |
| `hideserviceids` | query | `string` | no | Service(s) that should be hidden, if this service is selected |
| `uselogo` | query | `boolean` | no | True, if the the picture of this service should be used for the email logo |
| `severalcalendarsused` | query | `boolean` | no | True, if the service can only be booked if another calendar is available |
| `differenttimecombined` | query | `boolean` | no | True, if the service has a different time if booked with another service |
| `timeslotcombined` | query | `number` | no | Defines the time of the appointment if booked with another service. differenttimecombined has to be true |
| `tags` | query | `string` | no | ID of the tags that the contact gets after booking |
| `tagscancel` | query | `string` | no | ID of the tags that the contact gets after cancellation of the appointment |
| `externalreference` | query | `string` | no | Used for a tag ID or external reference after booking |
| `externalreferencedelete` | query | `string` | no | Used for a tag ID or external reference after cancellation of the appointment |
| `externalreferencechange` | query | `string` | no | Used for a tag ID or external reference after a change of the appointment |
| `externalreferencedate` | query | `string` | no | ID of a field that should contain the date of the appointment |
| `externalreferencelocation` | query | `string` | no | ID of a field that should contain the location of the appointment |
| `externalreferencecalname` | query | `string` | no | ID of a field that should contain the calendar name of the appointment |
| `externalreferencecancel` | query | `string` | no | ID of a field that should contain the cancellation link of the appointment |
| `jscode` | query | `string` | no | Used for JavaScript code that will be executed after the booking of the appointment (for example to redirect to another website) |
