# eTermin Universal API Examples

These examples use the MindCloud API key and eTermin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Calendars

Retrieves calendars from eTermin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendars?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "allAnswersSupported": true,
      "appInterval": 1,
      "calendarGroup": "string",
      "calendarId": 1,
      "calendarName": "Ava Chen",
      "calendarType": 1,
      "checkStartTimeOnlyWhenCapacity": true,
      "cluster": 1,
      "completeAppointmentWithinOpeningHours": true,
      "country": "string",
      "defaultAppDuration": 1,
      "defaultTimePattern": "string",
      "descriptionAr": "string",
      "descriptionBg": "string",
      "descriptionDe": "string",
      "descriptionEn": "string",
      "descriptionEs": "string",
      "descriptionFr": "string",
      "descriptionHu": "string",
      "descriptionIt": "string",
      "descriptionJa": "string",
      "descriptionNl": "string",
      "descriptionPl": "string",
      "descriptionPt": "string",
      "descriptionRu": "string",
      "differentIntervals": true,
      "differentLocation": true,
      "durationFactor": 1,
      "eMail": "ava@example.com",
      "eMailConfirmMsg": true,
      "eMailLocation": "ava@example.com",
      "eMailManualConfirm": "ava@example.com",
      "enableCapacity": true,
      "enabled": true,
      "externalReference": "string",
      "lastBookingDateTime": 1,
      "limitToDuration": true,
      "maxCapacity": 1,
      "maxDuration": 1,
      "minCapacity": 1,
      "mobilePhone": "string",
      "name": "Ava Chen",
      "severalLocations": true,
      "smsNotification": true,
      "smsPhoneNumber": "string",
      "smsTimeSpanHours": "string",
      "sortIdx": 1,
      "street": "string",
      "telephone": "string",
      "timeSlotMinutes": 1,
      "town": "string",
      "transparentMarkAsOccupied": true,
      "useReceiverAsSenderEmail": true,
      "waitingNr": true,
      "web": "string",
      "wnPrefix": "string",
      "wnStartNr": 1,
      "zip": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Calendars action reference](actions/list-calendars.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eTermin/latest/actions/list-calendars).

## Assign Calendar Services

Assigns services to a calendar in eTermin.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/assign-calendar-services" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendarid": "string",
  "serviceid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/assign-calendar-services', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendarid": "string",
    "serviceid": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Assign Calendar Services action reference](actions/assign-calendar-services.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eTermin/latest/actions/assign-calendar-services).
