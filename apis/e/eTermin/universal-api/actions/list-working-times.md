# eTermin: List Working Times

Retrieves working times from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-working-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-working-times?connectionId=$CONNECTION_ID&calendarid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-working-times?${params}`, {
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
| `all` | boolean | no | Use this parameter instead of calendarid, if you want the workingtimes of all calendars |
| `join` | number | no | Set to 1 for the same information but with names instead of numbers |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allServiceIDsRequired": 1,
      "calendarIntervalId": 1,
      "enabled": true,
      "endTime": "string",
      "id": 1,
      "locationId": 1,
      "serviceIDs": "string",
      "slotType": 1,
      "startTime": "string",
      "validWithServiceId": 1,
      "weekDay": "string",
      "weekDayIdx": 1,
      "weekType": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allServiceIDsRequired` | number |  |
| `calendarIntervalId` | number |  |
| `enabled` | boolean |  |
| `endTime` | string |  |
| `id` | number |  |
| `locationId` | number |  |
| `serviceIDs` | string |  |
| `slotType` | number |  |
| `startTime` | string |  |
| `validWithServiceId` | number |  |
| `weekDay` | string |  |
| `weekDayIdx` | number |  |
| `weekType` | number |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/workingtimes` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-working-times.md) for the provider-specific parameters and requirements.

