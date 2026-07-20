# eTermin: List Working Times by Date

Retrieves working times by date from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-working-times-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-working-times-by-date?connectionId=$CONNECTION_ID&calendarid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-working-times-by-date?${params}`, {
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
| `calendarid` | number | yes | CalendarID of the calendar you need the working times for |
| `join` | number | no | Set to 1 for the same information but with names instead of numbers |
| `start` | string | no | Start date from when the workingtimes should be shown. Format needs to be yyyy-mm-dd |
| `end` | string | no | End date until the workingtimes should be shown. Needs the start parameter. Format needs to be yyyy-mm-dd |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allServiceIDsRequired": 1,
      "calendarId": 1,
      "endDate": "string",
      "externalUid": "string",
      "id": 1,
      "locationId": 1,
      "locationName": "Ava Chen",
      "nrApps": 1,
      "oneOff": true,
      "oneOffCode": "string",
      "overwriteDay": true,
      "reason": "string",
      "serviceIDs": "string",
      "slotType": 1,
      "startDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allServiceIDsRequired` | number |  |
| `calendarId` | number |  |
| `endDate` | string |  |
| `externalUid` | string |  |
| `id` | number |  |
| `locationId` | number |  |
| `locationName` | string |  |
| `nrApps` | number |  |
| `oneOff` | boolean |  |
| `oneOffCode` | string |  |
| `overwriteDay` | boolean |  |
| `reason` | string |  |
| `serviceIDs` | string |  |
| `slotType` | number |  |
| `startDate` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/workingtimesdate` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-working-times-by-date.md) for the provider-specific parameters and requirements.

