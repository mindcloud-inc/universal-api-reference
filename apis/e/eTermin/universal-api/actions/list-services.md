# eTermin: List Services

Retrieves services from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-services?${params}`, {
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
| `languageid` | string | no | Use the language code in which you want the name and description of the service (e.g., DE, EN, etc.) |
| `id` | number | no | ID of the service to get the information of a specific service |
| `serviceGroupId` | number | no | Use if you want only services of a specific service group |
| `addimage` | number | no | true if you want to also get the image-data in your response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abbreviation": "string",
      "addAppHours": 1,
      "allowOnlyThisService": true,
      "appDeadline": 1,
      "appFuture": 1,
      "appointmentLocation": 1,
      "appointmentLocationText": "string",
      "bookingType": 1,
      "calendarSelection": 1,
      "cancelDeadline": 1,
      "capSelText": "string",
      "color": "string",
      "currency": 1,
      "currencyNew": 1,
      "cwa": 1,
      "daySelectionType": 1,
      "differentTimeCombined": true,
      "differentTimeResource": true,
      "emailTxt": "ava@example.com",
      "enableCapacity": true,
      "enabled": true,
      "externalReference": "string",
      "externalReferenceCancel": "string",
      "externalReferenceChange": "string",
      "externalReferenceDate": "string",
      "externalReferenceDelete": "string",
      "feedback": 1,
      "fillCalendarStrategy": 1,
      "foreColor": "string",
      "globalAnswerSortIdx": 1,
      "hideServiceIDs": 1,
      "info": "string",
      "infoTextInSlots": true,
      "infoTxtP2": "string",
      "jsCode": "string",
      "maxCapacity": 1,
      "maxCapacityUserSel": 1,
      "minCapacity": 1,
      "multiAppointment": 1,
      "multiplyPriceWithCap": true,
      "multiServiceDurationCalcMethod": 1,
      "multiServiceMax": 1,
      "multiServiceMin": 1,
      "multiServiceSel": true,
      "nrAppSel": 1,
      "nrAppSelAdjacent": true,
      "nrAppSelAdjacentType": 1,
      "nrTimeSlotEntries": 1,
      "paa": 1,
      "pap": 1,
      "pm0": 1,
      "pm1": 1,
      "pm2": 1,
      "price": 1,
      "priceInfoPos": 1,
      "priceIsPercentage": true,
      "priceSuffix": "string",
      "rRule": "string",
      "service": "string",
      "serviceGroupId": 1,
      "serviceId": 1,
      "severalCalendarsUsed": true,
      "showCapSelectionBox": true,
      "showInternal": true,
      "showServiceIDs": 1,
      "smsConfirmation": 1,
      "sortOrder": 1,
      "subQuestionId": 1,
      "tags": "string",
      "timeSlotCombined": 1,
      "timeSlotFormat": 1,
      "timeSlotMinutes": 1,
      "timeSlotMinutesResEnd": 1,
      "timeSlotMinutesResStart": 1,
      "vat": 1,
      "vendorConfirmation": 1,
      "voucherField": 1,
      "waitingList": 1,
      "workloadPerc": 1,
      "wowing": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abbreviation` | string |  |
| `addAppHours` | number |  |
| `allowOnlyThisService` | boolean |  |
| `appDeadline` | number |  |
| `appFuture` | number |  |
| `appointmentLocation` | number |  |
| `appointmentLocationText` | string |  |
| `bookingType` | number |  |
| `calendarSelection` | number |  |
| `cancelDeadline` | number |  |
| `capSelText` | string |  |
| `color` | string |  |
| `currency` | number |  |
| `currencyNew` | number |  |
| `cwa` | number |  |
| `daySelectionType` | number |  |
| `differentTimeCombined` | boolean |  |
| `differentTimeResource` | boolean |  |
| `emailTxt` | string |  |
| `enableCapacity` | boolean |  |
| `enabled` | boolean |  |
| `externalReference` | string |  |
| `externalReferenceCancel` | string |  |
| `externalReferenceChange` | string |  |
| `externalReferenceDate` | string |  |
| `externalReferenceDelete` | string |  |
| `feedback` | number |  |
| `fillCalendarStrategy` | number |  |
| `foreColor` | string |  |
| `globalAnswerSortIdx` | number |  |
| `hideServiceIDs` | number |  |
| `info` | string |  |
| `infoTextInSlots` | boolean |  |
| `infoTxtP2` | string |  |
| `jsCode` | string |  |
| `maxCapacity` | number |  |
| `maxCapacityUserSel` | number |  |
| `minCapacity` | number |  |
| `multiAppointment` | number |  |
| `multiplyPriceWithCap` | boolean |  |
| `multiServiceDurationCalcMethod` | number |  |
| `multiServiceMax` | number |  |
| `multiServiceMin` | number |  |
| `multiServiceSel` | boolean |  |
| `nrAppSel` | number |  |
| `nrAppSelAdjacent` | boolean |  |
| `nrAppSelAdjacentType` | number |  |
| `nrTimeSlotEntries` | number |  |
| `paa` | number |  |
| `pap` | number |  |
| `pm0` | number |  |
| `pm1` | number |  |
| `pm2` | number |  |
| `price` | number |  |
| `priceInfoPos` | number |  |
| `priceIsPercentage` | boolean |  |
| `priceSuffix` | string |  |
| `rRule` | string |  |
| `service` | string |  |
| `serviceGroupId` | number |  |
| `serviceId` | number |  |
| `severalCalendarsUsed` | boolean |  |
| `showCapSelectionBox` | boolean |  |
| `showInternal` | boolean |  |
| `showServiceIDs` | number |  |
| `smsConfirmation` | number |  |
| `sortOrder` | number |  |
| `subQuestionId` | number |  |
| `tags` | string |  |
| `timeSlotCombined` | number |  |
| `timeSlotFormat` | number |  |
| `timeSlotMinutes` | number |  |
| `timeSlotMinutesResEnd` | number |  |
| `timeSlotMinutesResStart` | number |  |
| `vat` | number |  |
| `vendorConfirmation` | number |  |
| `voucherField` | number |  |
| `waitingList` | number |  |
| `workloadPerc` | number |  |
| `wowing` | number |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/service` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

