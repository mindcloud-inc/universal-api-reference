# eTermin: Update Working Times by Date

Updates working times by date in eTermin.

```
PUT https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-working-times-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-working-times-by-date" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "start": "string",
  "end": "string",
  "calendarid": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-working-times-by-date', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "start": "string",
    "end": "string",
    "calendarid": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the working time that needs to be changed |
| `start` | string | yes | Start date/time of working time e.g. 2019-07-14 09:00 |
| `end` | string | yes | End date/time of working time e.g. 2019-07-14 18:00 |
| `calendarid` | number | yes | ID of the calendar |
| `reason` | string | no | Reason of the specific working time (this is only visible internally) |
| `slottype` | number | no | 0 if time slots should be valid for internal and external (online booked) appointments. 1 if timeslots are only valid for interal (manually entered) appointments |
| `nrapps` | number | no | Amount of appointments that are bookable in this working slot. (-1 = unlimited) |
| `overwriteday` | boolean | no | true, if the workingtime for this day should be disabled |
| `validwithserviceid` | string | no | List of services that work with this working slot |
| `allserviceidsrequired` | number | no | Defines how the validity of the services are checked. Exclusive means that only the services provided with the parameter validwithserviceid are allowed. If not exclusive, every service the calendar is activated for can be used. <br> 0 = one service needs to be selected <br> 1 = all services need to be selected exclusively <br> 2 = all services need to be selected <br> 3 = one service needs to be selected exclusively) |
| `locationid` | number | no | ID of the location for this working slot if locations are used in working times |
| `oneoff` | boolean | no | true, if this timeslot needs a specific link (requires exactly one service for the validwithserviceid parameter) |
| `oneoffcode` | string | no | Specific code that is used for the oneoff-link if oneoff is true |
| `waitinglist` | boolean | no | true, if this timeslot should be filled with appointments from the waitinglist |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "statusmsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `statusmsg` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `PUT /api/workingtimesdate` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-working-times-by-date.md) for the provider-specific parameters and requirements.

