# eTermin: List Available Time Slots

Retrieves available time slots from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-available-time-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-available-time-slots?connectionId=$CONNECTION_ID&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-available-time-slots?${params}`, {
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
| `date` | string | yes | Day that you want to check if there are available slots. Format: yyyy-mm-dd |
| `rangesearch` | number | no | 0 - All slots of a specific day will be displayed <br> 1 - Searches until it found a date when slots are available. Returns the number of slots that are available on a specific day |
| `end` | string | no | End date of the time range. Only works if rangesearch=1. Format: yyyy-mm-dd |
| `serviceid` | string | no | ID(s) of the selected service(s). This parameter is required if you restrict the calendar or working times to specific services. Several service ID's can be separated with a comma (,). e.g. 45345,45346 etc. |
| `calendarid` | string | no | ID of the calendar. Use this parameter if you want to get available time slots for a specific calendar. If this parameter is empty, available time slots for all calendars will be returned. |
| `capacity` | number | no | Defines the capacity that is searched for, if you have capacity enabled |
| `duration` | number | no | Appointment duration in minutes. Use this parameter if you want to use a different duration than specified for the service |
| `cluster` | number | no | Appointment cluster on (1) or off (0) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": "string",
      "adw": 1,
      "available": 1,
      "calendarid": 1,
      "calendarname": "Ava Chen",
      "cap": 1,
      "capmax": 1,
      "ecap": true,
      "end": "string",
      "f": true,
      "idandtimeslot": "string",
      "start": "string",
      "wl": 1,
      "wlend": 1,
      "wlstart": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | string |  |
| `adw` | number |  |
| `available` | number |  |
| `calendarid` | number |  |
| `calendarname` | string |  |
| `cap` | number |  |
| `capmax` | number |  |
| `ecap` | boolean |  |
| `end` | string |  |
| `f` | boolean |  |
| `idandtimeslot` | string |  |
| `start` | string |  |
| `wl` | number |  |
| `wlend` | number |  |
| `wlstart` | number |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/timeslots` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-time-slots.md) for the provider-specific parameters and requirements.

