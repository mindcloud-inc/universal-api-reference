# eTermin: List Calendars

Retrieves calendars from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `calendarid` | number | no | ID of the calendar, if you only need to get the details of a single calendar |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allAnswersSupported` | boolean |  |
| `appInterval` | number |  |
| `calendarGroup` | string |  |
| `calendarId` | number |  |
| `calendarName` | string |  |
| `calendarType` | number |  |
| `checkStartTimeOnlyWhenCapacity` | boolean |  |
| `cluster` | number |  |
| `completeAppointmentWithinOpeningHours` | boolean |  |
| `country` | string |  |
| `defaultAppDuration` | number |  |
| `defaultTimePattern` | string |  |
| `descriptionAr` | string |  |
| `descriptionBg` | string |  |
| `descriptionDe` | string |  |
| `descriptionEn` | string |  |
| `descriptionEs` | string |  |
| `descriptionFr` | string |  |
| `descriptionHu` | string |  |
| `descriptionIt` | string |  |
| `descriptionJa` | string |  |
| `descriptionNl` | string |  |
| `descriptionPl` | string |  |
| `descriptionPt` | string |  |
| `descriptionRu` | string |  |
| `differentIntervals` | boolean |  |
| `differentLocation` | boolean |  |
| `durationFactor` | number |  |
| `eMail` | string |  |
| `eMailConfirmMsg` | boolean |  |
| `eMailLocation` | string |  |
| `eMailManualConfirm` | string |  |
| `enableCapacity` | boolean |  |
| `enabled` | boolean |  |
| `externalReference` | string |  |
| `lastBookingDateTime` | number |  |
| `limitToDuration` | boolean |  |
| `maxCapacity` | number |  |
| `maxDuration` | number |  |
| `minCapacity` | number |  |
| `mobilePhone` | string |  |
| `name` | string |  |
| `severalLocations` | boolean |  |
| `smsNotification` | boolean |  |
| `smsPhoneNumber` | string |  |
| `smsTimeSpanHours` | string |  |
| `sortIdx` | number |  |
| `street` | string |  |
| `telephone` | string |  |
| `timeSlotMinutes` | number |  |
| `town` | string |  |
| `transparentMarkAsOccupied` | boolean |  |
| `useReceiverAsSenderEmail` | boolean |  |
| `waitingNr` | boolean |  |
| `web` | string |  |
| `wnPrefix` | string |  |
| `wnStartNr` | number |  |
| `zip` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/calendar` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendars.md) for the provider-specific parameters and requirements.

