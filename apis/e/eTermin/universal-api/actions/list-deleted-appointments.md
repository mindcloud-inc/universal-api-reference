# eTermin: List Deleted Appointments

Retrieves deleted appointments from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-deleted-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-deleted-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-deleted-appointments?${params}`, {
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
| `start` | date | no | Start day when appointment(s) got deleted. Format: yyyy-mm-dd. It will return a list with all appointments that are between start and end |
| `end` | date | no | End day when appointment(s) got deleted. Format: yyyy-mm-dd. It will return a list with all appointments there are between start and end |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": 1,
      "calendarid": 1,
      "calendarName": "Ava Chen",
      "customerNumber": "string",
      "deletedBy": "string",
      "email": "ava@example.com",
      "endDateTime": "string",
      "endDateTimeUtc": "string",
      "externalId": "string",
      "firstName": "Ava",
      "lastName": "Chen",
      "notes": "string",
      "phone": "string",
      "rc": 1,
      "servicesText": "string",
      "startDateTime": "string",
      "startDateTimeUtc": "string",
      "timeStamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | number |  |
| `calendarid` | number |  |
| `calendarName` | string |  |
| `customerNumber` | string |  |
| `deletedBy` | string |  |
| `email` | string |  |
| `endDateTime` | string |  |
| `endDateTimeUtc` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `rc` | number |  |
| `servicesText` | string |  |
| `startDateTime` | string |  |
| `startDateTimeUtc` | string |  |
| `timeStamp` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/appointmentdeleted` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deleted-appointments.md) for the provider-specific parameters and requirements.

