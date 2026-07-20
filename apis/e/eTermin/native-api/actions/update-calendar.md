# Update Calendar with eTermin

Updates an existing calendar in eTermin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/calendar`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Update Calendar](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Calendar/put_api_calendar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | ID of the calendar |
| `calendarname` | query | `string` | no | Name of the calendar. This name is used for all languages |
| `descriptionlanguagecode` | query | `string` | no | e.g. descriptionde adds additional information for this calendar in German language. descriptionen in English etc. |
| `descriptiondisplaytype` | query | `number` | no | defines if the description is shown on the bookingpage <br> 0 = not shown<br> 1 = shown under calendar name<br> 2 = shown as tooltip |
| `enablecapacity` | query | `boolean` | no | Several appointments can be booked at the same time |
| `maxcapacity` | query | `number` | no | Maximum capacity of appointments that can be booked at the same time |
| `differentlocation` | query | `boolean` | no | The location of the calendar is different than the main location |
| `name` | query | `string` | no | Name of the different company name |
| `street` | query | `string` | no | Street |
| `zip` | query | `string` | no | ZIP |
| `city` | query | `string` | no | City |
| `country` | query | `string` | no | Country |
| `telephone` | query | `string` | no | Telephone |
| `mobilephone` | query | `string` | no | MobilePhone |
| `emaillocation` | query | `string` | no | Email |
| `web` | query | `string` | no | Internet address |
| `completeappointmentwithinopeninghours` | query | `boolean` | no | If you have configured services where free, idle or down times between appointments occur, you can define whether these should be within the defined available times. |
| `smsnotification` | query | `boolean` | no | Employee will be informed by SMS if an appointment was booked |
| `smsphonenumber` | query | `string` | no | Number of the phone |
| `smstimespanhours` | query | `number` | no | Threshold (in hours) if SMS should be sent |
| `calendartype` | query | `boolean` | no | Main calendar (0) or sub calendar (1) |
| `limittoduration` | query | `number` | no | Calendar can only handle appointments that have a certain length (defined in maxduration) |
| `maxduration` | query | `number` | no | Maximum appointment duration (minutes) |
| `waitingnr` | query | `boolean` | no | Calculate waiting number |
| `wnprefix` | query | `string` | no | Prefix of the waiting number |
| `wnstartnr` | query | `number` | no | Start number of the waiting number |
