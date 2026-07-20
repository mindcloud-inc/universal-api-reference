# eTermin: List Appointments

Retrieves appointments from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-appointments?${params}`, {
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
| `appid` | number | no | ID of an appointment. (relates to the ID) |
| `id` | string | no | ID of an appointment. (relates to the ExternalID) |
| `start` | string | no | Start date of the appointments. Format yyyy-mm-dd. It will return a list with all appointments that are between "start" and "end". |
| `end` | string | no | End date of the appointments. Format yyyy-mm-dd. It will return a list with all appointments that are between "start" and "end". |
| `bycreationdate` | boolean | no | Changes the start and end parameters to look for the creation date instead of the date, the appointment takes place |
| `calendarid` | string | no | IDs of the calendars that you want to get appointments from, you can separate multiple calendars with a "," |
| `wl` | boolean | no | Set to 1 if you want to get all appointments on the Waiting List (start and end parameters required) |
| `pbl` | boolean | no | Set to 1 if you want to get all appointments on the Reservation List (start and end parameters not required) |
| `cid` | number | no | Use a customer ID to see all appointments that are related to this customer. (start and end parameters not required) |
| `email` | string | no | Use an email address to see all appointments that are related to this email. (start and end parameters required) |
| `limited` | boolean | no | Reduces the amount of information that the response have. Set to 1 if you want basic information about a lot of appointments. |
| `noholidays` | boolean | no | Only shows appointments that are no holidays and not blocked appointments. |
| `noholidays2` | boolean | no | Only shows appointments that are no holidays. (bookingtype <> "Holiday") |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additional1": "string",
      "additional10": "string",
      "additional11": "string",
      "additional12": "string",
      "additional13": "string",
      "additional14": "string",
      "additional15": "string",
      "additional16": "string",
      "additional17": "string",
      "additional18": "string",
      "additional19": "string",
      "additional2": "string",
      "additional20": "string",
      "additional3": "string",
      "additional4": "string",
      "additional5": "string",
      "additional6": "string",
      "additional7": "string",
      "additional8": "string",
      "additional9": "string",
      "appattrib": 1,
      "appCapacity": 1,
      "attachmentLink1": "https://example.com",
      "attachmentLink2": "https://example.com",
      "attachmentLink3": "https://example.com",
      "attachmentLink4": "https://example.com",
      "attachmentLink5": "https://example.com",
      "attachmentLink6": "https://example.com",
      "birthday": "string",
      "blockedApp": true,
      "bookingLanguage": "string",
      "bookingType": "string",
      "bookingTypeOriginal": "string",
      "bookingUrl": "https://example.com",
      "calendarId": 1,
      "calendarName": "Ava Chen",
      "calendarsSyncReadOnly": 1,
      "creationDate": "string",
      "customerNumber": "string",
      "email": "ava@example.com",
      "endDateTime": "string",
      "endDateTimeUtc": "string",
      "externalId": "string",
      "firstName": "Ava",
      "id": 1,
      "isReadOnly": true,
      "lastName": "Chen",
      "linkedAppId": 1,
      "location": "string",
      "manualConfirmed": 1,
      "multiAppId": 1,
      "notes": "string",
      "paymentMethod": 1,
      "phone": "string",
      "postTimeMin": 1,
      "preTimeMin": 1,
      "priceGross": 1,
      "recurrenceId": 1,
      "recurrenceParentId": 1,
      "recurrenceRule": "string",
      "recurrenceState": 1,
      "salutation": "string",
      "selectedAnswers": "string",
      "sequence": 1,
      "servicesCapacity": "string",
      "servicesText": "string",
      "severalTimeSlots": "string",
      "startDateTime": "string",
      "startDateTimeUtc": "string",
      "state": "string",
      "status": 1,
      "street": "string",
      "summaryCalDav": "string",
      "title": "string",
      "town": "string",
      "transactionId": "string",
      "voucherCode": "string",
      "voucherValue": 1,
      "waitNumber": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additional1` | string |  |
| `additional10` | string |  |
| `additional11` | string |  |
| `additional12` | string |  |
| `additional13` | string |  |
| `additional14` | string |  |
| `additional15` | string |  |
| `additional16` | string |  |
| `additional17` | string |  |
| `additional18` | string |  |
| `additional19` | string |  |
| `additional2` | string |  |
| `additional20` | string |  |
| `additional3` | string |  |
| `additional4` | string |  |
| `additional5` | string |  |
| `additional6` | string |  |
| `additional7` | string |  |
| `additional8` | string |  |
| `additional9` | string |  |
| `appattrib` | number |  |
| `appCapacity` | number |  |
| `attachmentLink1` | string |  |
| `attachmentLink2` | string |  |
| `attachmentLink3` | string |  |
| `attachmentLink4` | string |  |
| `attachmentLink5` | string |  |
| `attachmentLink6` | string |  |
| `birthday` | string |  |
| `blockedApp` | boolean |  |
| `bookingLanguage` | string |  |
| `bookingType` | string |  |
| `bookingTypeOriginal` | string |  |
| `bookingUrl` | string |  |
| `calendarId` | number |  |
| `calendarName` | string |  |
| `calendarsSyncReadOnly` | number |  |
| `creationDate` | string |  |
| `customerNumber` | string |  |
| `email` | string |  |
| `endDateTime` | string |  |
| `endDateTimeUtc` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `isReadOnly` | boolean |  |
| `lastName` | string |  |
| `linkedAppId` | number |  |
| `location` | string |  |
| `manualConfirmed` | number |  |
| `multiAppId` | number |  |
| `notes` | string |  |
| `paymentMethod` | number |  |
| `phone` | string |  |
| `postTimeMin` | number |  |
| `preTimeMin` | number |  |
| `priceGross` | number |  |
| `recurrenceId` | number |  |
| `recurrenceParentId` | number |  |
| `recurrenceRule` | string |  |
| `recurrenceState` | number |  |
| `salutation` | string |  |
| `selectedAnswers` | string |  |
| `sequence` | number |  |
| `servicesCapacity` | string |  |
| `servicesText` | string |  |
| `severalTimeSlots` | string |  |
| `startDateTime` | string |  |
| `startDateTimeUtc` | string |  |
| `state` | string |  |
| `status` | number |  |
| `street` | string |  |
| `summaryCalDav` | string |  |
| `title` | string |  |
| `town` | string |  |
| `transactionId` | string |  |
| `voucherCode` | string |  |
| `voucherValue` | number |  |
| `waitNumber` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/appointment` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointments.md) for the provider-specific parameters and requirements.

