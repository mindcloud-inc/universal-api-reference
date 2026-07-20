# eTermin: Sync Appointments

Retrieves appointment changes from eTermin using a sync token.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/sync-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/sync-appointments?connectionId=$CONNECTION_ID&synctoken=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "synctoken": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/sync-appointments?${params}`, {
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
| `synctoken` | number | yes | SyncToken. If you start the synchronization the first time, please use 1. eTermin will return a (new) SyncToken after each call. This value can be found in the header. Please use then the new SnycToken when you call the api function again. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "a10": "string",
      "a11": "string",
      "a12": "string",
      "a13": "string",
      "a14": "string",
      "a15": "string",
      "a16": "string",
      "a17": "string",
      "a18": "string",
      "a19": "string",
      "a20": "string",
      "a7": "string",
      "a8": "string",
      "a9": "string",
      "additional1": "string",
      "additional2": "string",
      "additional3": "string",
      "additional4": "string",
      "additional5": "string",
      "additional6": "string",
      "appAttrib": 1,
      "appCapacity": 1,
      "attachmentLink1": "https://example.com",
      "attachmentLink2": "https://example.com",
      "attachmentLink3": "https://example.com",
      "attachmentLink4": "https://example.com",
      "attachmentLink5": "https://example.com",
      "attachmentLink6": "https://example.com",
      "birthday": "string",
      "blockedApp": 1,
      "bookingDate": "string",
      "bookingDateUtc": "string",
      "bookingLanguage": "string",
      "bookingType": "string",
      "bookingTypeOriginal": "string",
      "calendarId": 1,
      "calendarsSyncReadOnly": 1,
      "contactId": 1,
      "creationDate": "string",
      "customerNumber": "string",
      "email": "ava@example.com",
      "endDateTime": "string",
      "endDateTimeUtc": "string",
      "externalId": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "linkedAppId": 1,
      "linkedMaster": true,
      "location": "string",
      "manualConfirmed": 1,
      "multiAppId": 1,
      "notes": "string",
      "phone": "string",
      "recurrenceId": "string",
      "recurrenceParentId": "string",
      "recurrenceRule": "string",
      "reference": "string",
      "salutation": "string",
      "selectedAnswers": "string",
      "sequence": 1,
      "serviceIDs": "string",
      "startDateTime": "string",
      "startDateTimeUtc": "string",
      "status": 1,
      "street": "string",
      "summaryCalDav": "string",
      "syncKey": 1,
      "syncStatus": "string",
      "title": "string",
      "town": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `a10` | string |  |
| `a11` | string |  |
| `a12` | string |  |
| `a13` | string |  |
| `a14` | string |  |
| `a15` | string |  |
| `a16` | string |  |
| `a17` | string |  |
| `a18` | string |  |
| `a19` | string |  |
| `a20` | string |  |
| `a7` | string |  |
| `a8` | string |  |
| `a9` | string |  |
| `additional1` | string |  |
| `additional2` | string |  |
| `additional3` | string |  |
| `additional4` | string |  |
| `additional5` | string |  |
| `additional6` | string |  |
| `appAttrib` | number |  |
| `appCapacity` | number |  |
| `attachmentLink1` | string |  |
| `attachmentLink2` | string |  |
| `attachmentLink3` | string |  |
| `attachmentLink4` | string |  |
| `attachmentLink5` | string |  |
| `attachmentLink6` | string |  |
| `birthday` | string |  |
| `blockedApp` | number |  |
| `bookingDate` | string |  |
| `bookingDateUtc` | string |  |
| `bookingLanguage` | string |  |
| `bookingType` | string |  |
| `bookingTypeOriginal` | string |  |
| `calendarId` | number |  |
| `calendarsSyncReadOnly` | number |  |
| `contactId` | number |  |
| `creationDate` | string |  |
| `customerNumber` | string |  |
| `email` | string |  |
| `endDateTime` | string |  |
| `endDateTimeUtc` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `linkedAppId` | number |  |
| `linkedMaster` | boolean |  |
| `location` | string |  |
| `manualConfirmed` | number |  |
| `multiAppId` | number |  |
| `notes` | string |  |
| `phone` | string |  |
| `recurrenceId` | string |  |
| `recurrenceParentId` | string |  |
| `recurrenceRule` | string |  |
| `reference` | string |  |
| `salutation` | string |  |
| `selectedAnswers` | string |  |
| `sequence` | number |  |
| `serviceIDs` | string |  |
| `startDateTime` | string |  |
| `startDateTimeUtc` | string |  |
| `status` | number |  |
| `street` | string |  |
| `summaryCalDav` | string |  |
| `syncKey` | number |  |
| `syncStatus` | string |  |
| `title` | string |  |
| `town` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/appointmentsync` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-appointments.md) for the provider-specific parameters and requirements.

