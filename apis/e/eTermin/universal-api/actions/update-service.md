# eTermin: Update Service

Updates an existing service in eTermin.

```
PUT https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the service |
| `servicegroupid` | number | no | ID of the service group |
| `servicede` | string | no | Name of the service in german. For other languages use serviceLANGUAGECODE e.g. serviceen |
| `timeslotminutes` | number | no | Duration of the service in minutes |
| `infode` | string | no | Additional description of the service in german. For other languages use serviceLANGUAGECODE e.g. infoen |
| `infodisplay` | number | no | Defines where the information is shown (0 = below service name, 1 = informationtext page 2, 2 = summary after booking, 3 = below service name and summary after booking) |
| `differenttimeresource` | boolean | no | True if you want to add pre- or post processing times |
| `timeslotminutesresstart` | number | no | Busy by minute (use negative number to have a pre-processing time) |
| `timeslotminutesresend` | number | no | Busy until minute (use a number greater than timeslotminutes to have a post-processing time) |
| `price` | number | no | Price of the service |
| `priceispercentage` | boolean | no | True if price is a percentage |
| `abbreviation` | string | no | abbreviation of the service |
| `enablecapacity` | boolean | no | True to enable the capacity of the service |
| `showcapselectionbox` | boolean | no | True if the customer is able to select the capacity |
| `maxcapacity` | number | no | Sets the maximum capacity of the service |
| `maxcapacityusersel` | number | no | Sets the maximum capacity the user can set on the booking page (needs showcapselectionbox to be true) |
| `capacitynonsel` | number | no | Sets the capacity if selected on the booking page (needs showcapselectionbox to be false) |
| `image` | string | no | Image of the service |
| `appdeadline` | number | no | Time the appointment must be booked in advance in minutes |
| `appfuture` | number | no | Time the appointment can be booked in the future in days |
| `startedapp` | number | no | Time the appointment can be booked if already started in minutes (has to be a negative value) |
| `canceldeadline` | number | no | Time the appointment can be cancelled in hours |
| `dayselectiontype` | number | no | Defines how page 2 shows the available days (0 = Calendar, 1 = list of days) |
| `appointmentlocation` | number | no | Defines the location of the appointment |
| `appointmentlocationtext` | string | no | Defines the location text if appointmentlocation = 3 |
| `vendorconfirmation` | number | no | Defines if the appointment provider needs to manually confirm the appointment (0 = manually, 1 = automatically) |
| `smsconfirmation` | number | no | Defines if a SMS confirmation is sent after booking (1 = enabled, 0 = disabled) |
| `reminderhours` | number | no | Defines when the first reminder is sent in hours (needs to be a negative value) |
| `reminderhours2` | number | no | Defines when the second reminder is sent in hours (needs to be a negative value) |
| `cluster` | number | no | Defines if the cluster is applied to this service (1 = enabled, 0 = disabled) |
| `customerconfirm` | number | no | Defines if the customer needs to confirm the appointment (1 = enabled, 0 = disabled; doesn't work with online payments or vendorconfirmation) |
| `customerconfirmtime` | number | no | Time in minutes the customer has time to confirm the appointment (customerconfirm must be set to 1) |
| `pm0` | number | no | Shows online payment options (1 = enabled, 0 = disabled) |
| `pm1` | number | no | Shows on site payment options (1 = enabled, 0 = disabled) |
| `pm2` | number | no | Shows by invoice payment options (1 = enabled, 0 = disabled) |
| `paymentamountpercentage` | number | no | Defines the payment amount that needs to be paid at the end of booking |
| `paymentamountisabsolute` | number | no | Defines if paymentamountpercentage is abolute or a percentage (1 = absolute, 0 = percentage) |
| `currency` | string | no | Defines the currency of the service |
| `voucherfield` | number | no | Defines if the voucherfield is shown (0 = not shown, 1 = shown, 2 = shown and mandatory) |
| `mpbs` | number | no | Defines if the price is multiplied by the amount of booked appointments |
| `timeslotformat` | number | no | Defines how the timeslots are shown on page 2 on the bookingpage (0 = starttime - endtime, 1 = starttime, 2 = only date, 3 = calendar week, 4 = like 0 but with dates, 5 = startdate only) |
| `multiappointment` | number | no | Defines if multiple appointments can be booked in one booking (0 = no, 1 = yes) |
| `multiservicedurationcalcmethod` | number | no | Defines how the duration is calculated if multiple services are selected (0 = all durations are summed up, 1 = only duration of the longest service, 2 = all durations are halfed, 3 = like 2 except the longest service) |
| `calendarselection` | number | no | Defines if the calendar selection should be shown (0 = no, 1 = yes) |
| `ssca` | number | no | Defines if in the calendar selection the entry all calendars is shown (0 = no, 1 = yes) |
| `showcalname` | number | no | Defines if in the calendar name is shown in the time slot (0 = no, 1 = yes) |
| `showcalpic` | number | no | Defines if in the calendar picture is shown after the timeslot is selected (0 = no, 1 = yes) |
| `showavcap` | number | no | Defines if the available capacity is shown in time slots (0 = no, 1 = yes) |
| `limitbooking` | number | no | Defines if this service can be booked a limited amount of times per customer (0 = no, 1 = yes) |
| `limitappointmentstype` | number | no | Defines how the appointments are limited (0 = per booking day, 1 = per week, 2 = per month, 3 = per year, 4 = per booked day) |
| `limitappointments` | number | no | Defines how many appointments can be booked per customer |
| `limitservice` | number | no | Defines if the limitation only applies to this specific service |
| `wowing` | number | no | Set to 0 if the Wowing interface should be disabled for this service |
| `wowingautomationid` | number | no | Defines the Woing Automation ID |
| `paymentduration` | number | no | Defines the payment term for LexOffice |
| `workloadperc` | number | no | Defines the percentage of time slots that are not shown |
| `nrtimeslotentries` | number | no | Defines the maximum amount of time slots that are shown |
| `feedback` | number | no | Set to 0 if the feedback checkbox should not be shown |
| `calcdrivingtime` | number | no | Defines if driving time should be calculated (0 = no, 1 = yes) |
| `fillcalendarstrategy` | number | no | Defines how the calender should be filled (0 = standard, 1 = random, 2 = round Robin, 3 = sequential, 4 = skills, 5 = strict round Robin) |
| `waitinglist` | number | no | Defines if the waiting list should be available (0 = no, 1 = yes) |
| `notearlyapp` | number | no | Defines if the customer should get an email if an earlier appointment is available (0 = not active, 1 = for appointments that were cancelled online, 2 = for appointments cancelled online and manually, 3 = like 1 but per calendar, 4 = like 2 but per calendar) |
| `sortorder` | number | no | Defines the position in the servicegroup |
| `bookingtype` | number | no | Defines the bookingtype (0 = appointment, 1 = no appointment booking allowed, 2 = 'negative' appointment, 3 = reservation list, 4 = voucher sale) |
| `showinternal` | boolean | no | Defines if the service is shown in the backend |
| `enabled` | boolean | no | Defines if the service is shown in the frontend |
| `showindb` | boolean | no | Defines if the service is shown in the most booked area of the Dashboard |
| `emailsender` | string | no | Defines the sender adress of the email for this service |
| `emailtxtde` | string | no | A special placeholder %SERVICETEXT% for emails, use other language codes to set the text (for example emailtxten for english) |
| `infotxtp2` | string | no | A special placeholder %INFOTEXTP2% for page 2 of the booking page |
| `pricesuffixde` | string | no | Additional information for the price, use other language codes to set the text (for example emailtxten for english) |
| `priceinfopos` | number | no | Defines where the pricesuffix is shown (0 = left side, 1 = right side) |
| `vat` | number | no | Defines the vat rate of the service |
| `multiplypricewithcap` | boolean | no | Defines if the price is multiplied with the capacity |
| `pricediffperday` | boolean | no | Defines if different prices per weekday are applied |
| `issubscription` | boolean | no | Defines if the service is a subscription |
| `capseltextde` | string | no | Defines the text if there is a capacity selection on that service, use other language codes to set the text (for example capseltexten for english) |
| `mstextpos` | number | no | Defines the position of capseltext (0 = above selection, 1 = to the right) |
| `allowonlythisservice` | boolean | no | If there are multiple services with capacity available at the same time, this option prevents that they will get mixed, if set to true |
| `multiservicesel` | boolean | no | True, if the service can be booked multiple times after another. This won't work if the parameter enablecapacity is true aswell |
| `multiservicemin` | number | no | Defines the minimum amount that can be choosen for multi service selection |
| `multiservicemax` | number | no | Defines the maximum amount that can be choosen for multi service selection |
| `extramin` | number | no | Defines total wrap up time |
| `extramintype` | number | no | 0 if extramin should not be applied if differenttimeresource is true, 1 if extramin should be added to timeslotminutesresend |
| `maxappsel` | number | no | Defines the maximum amount of appointments that can be selected on the booking page if multiappointment is true (in this service or globally) |
| `nrappsel` | number | no | Defines the maximum / minimum amount of appointments that MUST be selected on the booking page if multiappointment is true (in this service or globally) |
| `maxminslots` | boolean | no | Defines if nrappsel is maximum (0) or minimum (1) |
| `nrappseladjacent` | boolean | no | True, if the selected appointments have to be adjacent |
| `nrappseladjacenttype` | number | no | 0 = the date and time need to be adjacent, 1 = only the day need to be adjacent |
| `specificrangenextslot` | boolean | no | True, if the next appointment needs to be after a specific timeframe |
| `rangestart` | number | no | Days after the last appoinment |
| `rangeend` | number | no | Days range for the new appointment |
| `infotextinslots` | boolean | no | True, if the info text should be shown in the slot text in page 2 of the booking page |
| `appattrib` | number | no | Defines which attribute is set automatically in appointment. Attributes are binary encoded (1st attribute = 1, 2nd = 2, 3rd = 4; 1st + 2nd = 3) |
| `addapphours` | number | no | Hours after the first appointment, where a second appointment is booked |
| `rrule` | string | no | Defines the RRULE for this service |
| `bookingminute` | number | no | Defines when the timeslots are shown (61 = no restrictions, 0 = every full hour, 31 = every full and half hour, 15 or 30 or 45 = x minutes after a full hour) |
| `showserviceids` | string | no | Service(s) that have to be selected to show this service |
| `hideserviceids` | string | no | Service(s) that should be hidden, if this service is selected |
| `uselogo` | boolean | no | True, if the the picture of this service should be used for the email logo |
| `severalcalendarsused` | boolean | no | True, if the service can only be booked if another calendar is available |
| `differenttimecombined` | boolean | no | True, if the service has a different time if booked with another service |
| `timeslotcombined` | number | no | Defines the time of the appointment if booked with another service. differenttimecombined has to be true |
| `tags` | string | no | ID of the tags that the contact gets after booking |
| `tagscancel` | string | no | ID of the tags that the contact gets after cancellation of the appointment |
| `externalreference` | string | no | Used for a tag ID or external reference after booking |
| `externalreferencedelete` | string | no | Used for a tag ID or external reference after cancellation of the appointment |
| `externalreferencechange` | string | no | Used for a tag ID or external reference after a change of the appointment |
| `externalreferencedate` | string | no | ID of a field that should contain the date of the appointment |
| `externalreferencelocation` | string | no | ID of a field that should contain the location of the appointment |
| `externalreferencecalname` | string | no | ID of a field that should contain the calendar name of the appointment |
| `externalreferencecancel` | string | no | ID of a field that should contain the cancellation link of the appointment |
| `jscode` | string | no | Used for JavaScript code that will be executed after the booking of the appointment (for example to redirect to another website) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "status": 1,
      "statusMsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `status` | number |  |
| `statusMsg` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `PUT /api/service` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service.md) for the provider-specific parameters and requirements.

