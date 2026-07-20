# eTermin: Update Appointment

Updates an existing appointment in eTermin.

```
PUT https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-appointment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the appointment that you want to modify. |
| `start` | date | no | Start date and time of the appointment. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `end` | date | no | End date and time of the appointment. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 19:00 |
| `calendarid` | number | no | ID of the calendar. |
| `calendarname` | string | no | Name of the calendar (needed for Webpush) |
| `services` | string | no | ID of the service. Use the 'Service - Get service details' function to get a list with all available services. To use multiple services use a comma (,) to seperate the IDs |
| `servicestext` | string | no | Name of the services |
| `servicesinclsgtext` | string | no | Name of the services including the service groups |
| `servicesabb` | string | no | Abbreviation of the services |
| `capacity` | number | no | Defines the capacity of the appointment |
| `location` | string | no | Location of the appointment |
| `manualconfirmed` | number | no | Set to 0 to have the appointment manually confirmed by the appoinment provider, set to 1 if the appointment got confirmed |
| `sendemail` | boolean | no | Send a confirmation email to the adress that was specified in the email parameter (1 = yes, 0 = no). |
| `msgtype` | boolean | no | ID of the template that is sent to the customer with the API call |
| `notificationmsg` | boolean | no | Send an information email to the appointment provider (1 = yes, 0 = no). |
| `sync` | boolean | no | True if the appointment should be synchronized with external calendars (1 = yes, 0 = no). |
| `appointmentreminderhours` | number | no | Defines when the first reminder is sent in hours (needs to be a negative value) |
| `appointmentreminderhours2` | number | no | Defines when the second reminder is sent in hours (needs to be a negative value) |
| `canceldeadline` | number | no | Minutes how long before the startdate the appointment can be cancelled |
| `recurrencerule` | string | no | Recurrence rule. e.g. DTSTART:20171126T083000Z DTEND:20181126T090000Z RRULE:FREQ=WEEKLY;INTERVAL=1;BYDAY=WE; |
| `pricegross` | number | no | Price including vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `pricenet` | number | no | Price excluding vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `vat` | number | no | Vat multiplied by 100 (e.g. 18.50€ = 1850) |
| `linkedappidmanual` | number | no | AppID of the linked app if the calendar linking should be applied after two appointments are booked. Keep in mind to update the second appointment aswell |
| `salutation` | string | no | Salutation of the person. |
| `title` | string | no | Title of the person. |
| `lastname` | string | no | Lastname of the person. |
| `firstname` | string | no | Firstname of the person. |
| `email` | string | no | E-Mail of the person. |
| `phone` | string | no | Phone of the person. |
| `company` | string | no | Company of the person (make sure this field exists in your account) |
| `notes` | string | no | Appointment notes. |
| `street` | string | no | Street. |
| `zip` | string | no | Zip. |
| `city` | string | no | City. |
| `customernumber` | string | no | ID of the person that booked appointment. |
| `additional1` | string | no | Additional appointment field 1. |
| `additional2` | string | no | Additional appointment field 2. |
| `additional3` | string | no | Additional appointment field 3. |
| `additional4` | string | no | Additional appointment field 4. |
| `additional5` | string | no | Additional appointment field 5. |
| `additional6` | string | no | Additional appointment field 6. |
| `additional7` | string | no | Additional appointment field 7. |
| `additional8` | string | no | Additional appointment field 8. |
| `additional9` | string | no | Additional appointment field 9. |
| `additional10` | string | no | Additional appointment field 10. |
| `additional11` | string | no | Additional appointment field 11. |
| `additional12` | string | no | Additional appointment field 12. |
| `additional13` | string | no | Additional appointment field 13. |
| `additional14` | string | no | Additional appointment field 14. |
| `additional15` | string | no | Additional appointment field 15. |
| `additional16` | string | no | Additional appointment field 16. |
| `additional17` | string | no | Additional appointment field 17. |
| `additional18` | string | no | Additional appointment field 18. |
| `additional19` | string | no | Additional appointment field 19. |
| `additional20` | string | no | Additional appointment field 20. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eTermin API returns.

## Native endpoint

Through the native eTermin API, this operation is `PUT /api/appointment` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-appointment.md) for the provider-specific parameters and requirements.

