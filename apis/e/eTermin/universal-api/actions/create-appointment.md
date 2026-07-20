# eTermin: Create Appointment

Creates a new appointment in eTermin.

```
POST https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "start": "string",
  "end": "string",
  "calendarid": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "start": "string",
    "end": "string",
    "calendarid": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | string | yes | Start date and time of the appointment. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `end` | string | yes | End date and time of the appointment. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 19:00 |
| `calendarid` | number | yes | ID of the calendar. Use the 'Calendar - Get calendar details' function to get a list with all available calendars |
| `calendarname` | string | no | Name of the calendar (needed for Webpush) |
| `services` | string | no | ID of the service. Use the 'Service - Get service details' function to get a list with all available services. To use multiple services use a comma (,) to seperate the IDs |
| `servicestext` | string | no | Name of the services |
| `servicesinclsgtext` | string | no | Name of the services including the service groups |
| `servicesabb` | string | no | Abbreviation of the services |
| `capacity` | number | no | Defines the capacity of the appointment |
| `capused` | boolean | no | true if the capacity of the appointment needs to be checked |
| `capmaxused` | number | no | Maximum capacity that can't be exceeded |
| `location` | string | no | Location of the appointment |
| `bookingtype` | string | no | Information about how the appointment is booked |
| `bookingurl` | string | no | Information from which URL the appointment got booked |
| `checkexist` | boolean | no | Checks if the appointment start/end time is available (1 = yes, 0 = no). May not work with multiple capacity |
| `manualconfirmed` | number | no | Set to 0 to have the appointment manually confirmed by the appoinment provider |
| `confirmappointment` | number | no | Set to 1 to have the appointment manually confirmed by the booker, won't work if manualconfirmed is set to 0 |
| `confirmtime` | number | no | Time in minutes that the booker is able to confirm the appointment before it gets deleted |
| `language` | string | no | Languagecode, defines in which language the emails are sent |
| `sendemail` | boolean | no | Send a confirmation email to the adress that was specified in the email parameter (1 = yes, 0 = no) |
| `sms` | boolean | no | Send a confirmation sms to the phone number that was specified in the phone field (1 = yes, 0 = no). |
| `notificationmsg` | boolean | no | Send an information email to the appointment provider (1 = yes, 0 = no). |
| `sync` | boolean | no | True if the appointment should be synchronized with external calendars (1 = yes, 0 = no). |
| `calselid` | number | no | Use this parameter with the value -1 to also use the Calendar Linking function (also requires a valid value for the parameter services) |
| `appointmentreminderhours` | number | no | Defines when the first reminder is sent in hours (needs to be a negative value) |
| `appointmentreminderhours2` | number | no | Defines when the second reminder is sent in hours (needs to be a negative value) |
| `canceldeadline` | number | no | Minutes how long before the startdate the appointment can be cancelled |
| `recurrencerule` | string | no | Recurrence rule. e.g. DTSTART:{20171126T083000Z} DTEND:{20171126T090000Z} RRULE:FREQ=WEEKLY;INTERVAL=1;BYDAY=WE; |
| `recurrenceparentid` | string | no | ID of the parent recurring appointment |
| `pricegross` | number | no | Price including vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `pricenet` | number | no | Price excluding vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `vat` | number | no | Vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `salutation` | string | no | Salutation of the person |
| `title` | string | no | Title of the person |
| `lastname` | string | no | Lastname of the person |
| `firstname` | string | no | Firstname of the person |
| `email` | string | no | E-Mail of the person |
| `phone` | string | no | Phone of the person |
| `company` | string | no | Company of the person (make sure this field exists in your account) |
| `notes` | string | no | Appointment notes |
| `street` | string | no | Street of the person that booked appointment |
| `zip` | string | no | Zip of the person that booked appointment |
| `city` | string | no | City of the person that booked appointment |
| `customernumber` | string | no | ID of the person that booked appointment |
| `birthday` | string | no | Date of birth of the person that booked appointment |
| `additional1` | string | no | Additional appointment field 1 |
| `additional2` | string | no | Additional appointment field 2 |
| `additional3` | string | no | Additional appointment field 3 |
| `additional4` | string | no | Additional appointment field 4 |
| `additional5` | string | no | Additional appointment field 5 |
| `additional6` | string | no | Additional appointment field 6 |
| `additional7` | string | no | Additional appointment field 7 |
| `additional8` | string | no | Additional appointment field 8 |
| `additional9` | string | no | Additional appointment field 9 |
| `additional10` | string | no | Additional appointment field 10 |
| `additional11` | string | no | Additional appointment field 11 |
| `additional12` | string | no | Additional appointment field 12 |
| `additional13` | string | no | Additional appointment field 13 |
| `additional14` | string | no | Additional appointment field 14 |
| `additional15` | string | no | Additional appointment field 15 |
| `additional16` | string | no | Additional appointment field 16 |
| `additional17` | string | no | Additional appointment field 17 |
| `additional18` | string | no | Additional appointment field 18 |
| `additional19` | string | no | Additional appointment field 19 |
| `additional20` | string | no | Additional appointment field 20 |
| `agbaccepted` | boolean | no | true if customer accepted the terms of service |
| `dataprivacyaccepted` | boolean | no | true if customer accepted the privacy terms |
| `feedbackpermissionaccepted` | boolean | no | true if the customer should get a feedback mail |
| `newsletter` | boolean | no | true if the customer accepted to get newsletters |
| `bookerinfo` | string | no | Parameter that includes information for the notification message to the appointment provider |
| `emailm` | number | no | Checks if there is an email, if set to 1 |
| `lnm` | number | no | Checks if there is a lastname, if set to 1 |
| `blacklist` | number | no | Checks if the email is on the blacklist, if set to 1 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalInformation": "string",
      "id": "string",
      "iid": 1,
      "iide": "string",
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
| `additionalInformation` | string |  |
| `id` | string |  |
| `iid` | number |  |
| `iide` | string |  |
| `status` | number |  |
| `statusMsg` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `POST /api/appointment` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-appointment.md) for the provider-specific parameters and requirements.

